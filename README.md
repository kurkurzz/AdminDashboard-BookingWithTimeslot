# TeleBot-AdminDashboard
Admin dashboard for telegram bot booking system.

Checkout the Telegram bot script in https://github.com/kurkurzz/TelegramBot-BookingWithTimeslot.

![Webp net-resizeimage (3)](https://user-images.githubusercontent.com/64152220/97802072-e6ea8a00-1bf5-11eb-9cb1-51ac415e9e3d.png)

## Technology Used
- Python PyQT5 (gui)
- Cloud Firestore (database)

## Steps to Recreate

#### 1. Clone this repository

#### 2. Install required packages in ```requirements.txt```.
- In the project directory terminal, run command:
  
        $ pip install -r requirements.txt

#### 3. Get ```firebase_adminsdk.json``` file.

- Create a Firebase account https://firebase.google.com (might need to insert billing information but don't worry it's still free).

- Go to Firebase console and click ```add project```.

- Give the project a name.

##### In ```Cloud Firestore``` tab.
- Click ```Create database```.

- Select ```Production Mode``` and click ```Next```.
 
  ![Webp net-resizeimage](https://user-images.githubusercontent.com/64152220/97683979-c84d8d00-1a55-11eb-918b-9da3ec8232e7.png)

- Go to ```Rules``` tab and change the ```false``` to ```true```.
  
  ![Screenshot (33)_LI](https://user-images.githubusercontent.com/64152220/97685620-53c71e00-1a56-11eb-91aa-0b180e05e34d.jpg)

##### In ```Settings``` tab.

- Go to ```Service Accounts```.

- Click ```Generate New Private Key```.
  
  ![Webp net-resizeimage (3)](https://user-images.githubusercontent.com/64152220/97688492-70178a80-1a57-11eb-96d0-94e97b88a016.png)

- A file will be downloaded. Rename the file name to ```firebase-adminsdk.json```.

- Insert the file in project directory.

###### Note: This is a private key that will be generated every time you download it. Please make sure it is the same file with the bot script's file (if applicable).

#### 4. Run ```main.py``` to run the script
- In project directory terminal, run command:
  
        $ python main.py

#### 5. Convert to .exe

- Copy all files from ```hook-files``` folder.
- Locate your pyinstaller's hooks folder. Example ```C:\Program Files\Python38\Lib\site-packages\PyInstaller\hooks```
  
-  Paste it in there.

- In project directory terminal, run command:
  
      pyinstaller -w -F -i 'icons\admin_icon.ico' main.py
- Lastly, copy ```firebase-adminsdk.json``` to the .exe directory.

- Done


## To Do
- [x] Find way to convert to .exe
- [ ] Auto refresh list when data changes happen.
