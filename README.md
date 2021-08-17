# Cracking Windows 7/8/8.1/10/11 Passwords
## _This Walkthrough is for Educational Purpose ONLY!_ [![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

##### Setting Up The Environment:
 - Create a bootable **Ubuntu Live USB**
 - MAC OS User(s) [Click Here!](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu)
 - Windows User(s) [Click Here!](https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview)
 - Ubuntu User(s) [Click Here!](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu)

### Once the Installation is complete Boot into Live USB
  - Windows User(s) [Click Here!](https://ubuntu.com/tutorials/try-ubuntu-before-you-install#1-getting-started)
  - Mac OS User(s) [Click Here!](https://ubuntu.com/tutorials/create-a-usb-stick-on-macos#7-boot-your-mac)

Once the Environment is all setup, You should be on your UBUNTU Live USB Desktop, Please following the following steps.

## Run Updates and Install the Following Package:
```sh
sudo apt-get update
sudo apt-get install chntpw
```

Once Installation is completed Mount your C: drive and navigate to the following **PATH** via terminal:
Note: _(Replace `{your-disk-volume-name}` With Your mounted drive name)_
```sh
cd /media/ubuntu/{your-disk-volume-name}/Windows/System32/config/
```

Run Following Command to see all the users on the Windows OS:
```sh
sudo chntpw -l SAM
```
![Command Above's Output Screenshot - 01](https://i.imgur.com/XLUTqR5.png)

Now You Need to Install in my case I want to remove password that I forgot on user account name `Tom`

> Use following command to Remove User Password:
```sh
chntpw -u Tom SAM
```
![Command Above's Output Screenshot - 02](https://i.imgur.com/6qgk9lP.png)

> When you are prompted Choose Option 1:

![Command Above's Output Screenshot - 03](https://i.imgur.com/pRXWF04.png)

> Now type `q` to quit user editing menu:

![Command Above's Output Screenshot - 03](https://i.imgur.com/ieDsXWa.png)


> Then type `y` to confirm and save the changes.

![Command Above's Output Screenshot - 03](https://i.imgur.com/zTodRj7.png)

Once done, type the following command and remove the UBUNTU LIVE Installation media:

```sh
sudo reboot now
```
> Your Computer Will Now Boot and Your User will be able to login without password.

# ✨YAAY!! You've Done IT!!!! ✨
