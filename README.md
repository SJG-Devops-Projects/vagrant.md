# Vagrant Usage and Virtual Environment Management
--------------------------------------------------
This project demonstrate the understanding of Vagrant by setting up and managing a development environment using Vagrant. This task shows the conpetence in creating, configuring and managing virtual environments. 
## Task Description:
### 1. Install Vagrant and VirtualBox
   
Search for virtualbox on google. Click on the download button on the displayed page.
 ![Screenshot 2024-08-19 090445](https://github.com/user-attachments/assets/9bb04cb0-928e-4f43-8551-1d0c5ac102c7)

Select your desired operating system to download the exe file on your system.

![Screenshot 2024-08-11 190537](https://github.com/user-attachments/assets/19bd9802-a42d-4347-a214-19a5dafab034)

Follow the prompt to install on your system.

![Screenshot 2024-08-18 195355](https://github.com/user-attachments/assets/0317cf98-2e2e-4081-82cf-516870d3bf27)

When asked if you want the app to make changes on your device, click "yes".

![Screenshot 2024-08-19 094501](https://github.com/user-attachments/assets/194ce982-46e4-42cc-a4e8-379a705bb0d0)

The Virtualbox installation will start.

![Screenshot 2024-08-19 094852](https://github.com/user-attachments/assets/ed51a57b-6676-48aa-af25-366ed8888177)

You might get a warning asking if you would like virtualbox to install the device software on your Windows operating system, click install. 


![Screenshot 2024-08-19 094933](https://github.com/user-attachments/assets/ba7c2330-66a0-45a4-9500-c84ded3ec1fd)

Once the installation is completed, click the finish button to exit the setup wizard and launch your virtualbox.

![Screenshot 2024-08-19 102922](https://github.com/user-attachments/assets/8f4c21cb-82e1-4be6-8a72-2e7237114c21)

Next, search for Vagrant on Google to download it. Click on Vagrant by Hashicorp.

![Screenshot 2024-08-21 113107](https://github.com/user-attachments/assets/ea89efb3-0251-4412-a427-5a7b5957c4f7)

Click on the download button.

![Screenshot 2024-08-21 113130](https://github.com/user-attachments/assets/2f25fed3-d7e6-40be-adb2-af0f49cdc91b)

Select and click the appropriate binary for your operating system.

![Screenshot 2024-08-08 125655](https://github.com/user-attachments/assets/b94f5626-2df4-42ec-a24f-88c6e4d9d6e9)

Accept the terms and click on install.

![Screenshot 2024-08-08 125758](https://github.com/user-attachments/assets/8a543639-f3f6-4edc-9086-6bc00a8c524f)

The installation will start and once it is completed, you have Vagrant installed on your system.

![Screenshot 2024-08-08 125834](https://github.com/user-attachments/assets/72a3286a-1fd2-421d-b90e-9fc8ae4eda0f)

### 2.Create a Vagrant Project 

To start with, open a location on your system eg. desktop. Right-click on a space, move your cursor down to NEW, then move the cursor to the right to click on Folder to create a folder. Give your folder a name.

![Screenshot 2024-08-21 143342](https://github.com/user-attachments/assets/a5ae174f-c5d0-43b2-90bb-35c42f449b10)

Open your newly created folder, right click and then scroll down to open in terminal. once your terminal is opened, type in code and hit on the enter button.This would open your visual studio code (you must have downloaded the visual studio code on your computer)

![Screenshot 2024-08-21 142659](https://github.com/user-attachments/assets/7497015c-d53d-42a3-9f8b-6284df854766)



![Screenshot 2024-08-21 160532](https://github.com/user-attachments/assets/89dd71cb-25d4-4c6e-a2dd-b89364955ea4)

Click on Terminal, then New Terminal to open your terminal on VS Code.

![Screenshot 2024-08-21 164809](https://github.com/user-attachments/assets/6d8bedc3-d261-45bf-a495-42a163e646dd)

Click on the dropdown arrow and select Git bash or any other terminal of your choice.

![Screenshot 2024-08-21 164850](https://github.com/user-attachments/assets/a22580cd-f0aa-4a82-9499-6dc7bb7cdaa5)


Create a Vagrantfile by initializing Vagrant and indicating the base box with the code below.

``` 
Vagrant init ubuntu/bionic64
```

![Screenshot 2024-08-21 161335](https://github.com/user-attachments/assets/24f27a10-0806-44c7-9113-6cc4249bf13d)

A Vagrantfile will be created inside your folder.

![Screenshot 2024-08-11 213523](https://github.com/user-attachments/assets/4c2bc116-b18c-459e-a7e2-4d60b545f642)

Search for Vagrantfile Generator on your search engine.


![Screenshot 2024-08-11 192333](https://github.com/user-attachments/assets/06899ed3-66fe-4c94-8127-b0aaad381774)

Type in and select the following to generate Vagrant configuration file.

Base box: ubuntu/bionic64

Provider: Virtualbox

Memory: 512 MB

CPUs: 1 cores

![Screenshot 2024-08-21 165602](https://github.com/user-attachments/assets/c432af28-52cb-4aff-9dbd-3b9e6bc2f9af)



![Screenshot 2024-08-21 175306](https://github.com/user-attachments/assets/c249ac28-e8c0-43b7-abc3-4105c20ca326)



![Screenshot 2024-08-21 170707](https://github.com/user-attachments/assets/319e089c-2124-4955-9df6-3f7d90281030)

Copy the generated configuration file into your Vagrantfile on your VS Code and save.

![Screenshot 2024-08-11 213453](https://github.com/user-attachments/assets/05472675-8432-4a27-a512-41dc7ba8e370)

Type the code below on your terminal to create and provision the guest machine.

```
vagrant up
 ```

![Screenshot 2024-08-11 213703](https://github.com/user-attachments/assets/cf0d6497-e1a5-49e4-ac77-5ef7c27fc027)

Check if the virtual machine is running with the code below.

```
vagrant status
```
![Screenshot 2024-08-11 213734](https://github.com/user-attachments/assets/eeb4ab86-6c3f-4d28-9d91-4990a67e96d5)

Next is the network. To forward port 8080 on the host to port 80 on the guest, type the code below in your vagrantfile and save.

```
config.vm.network "forwarded_port", guest: 80, host: 8080
```

![Screenshot 2024-08-11 215352](https://github.com/user-attachments/assets/bfcbbca6-e11b-4115-abb5-a1fdc4dded35)

Type vagrant up on your terminal, to provision the code.

![Screenshot 2024-08-11 215450](https://github.com/user-attachments/assets/8438b3b6-9476-4696-995d-5e51dc49683f)

### 3. Provision the Virtual Machine.

Provisioning a virtual machine in Vagrant allows you to automatically install software, adjust configurations. Provisioning can be done manually but using the provisioning systems built-in to Vagrant, automates the process so that it is repeatable. Most importantly, it requires no human intervension, you can have a fully ready-to-go work environment with a single command.

Provisioning the virtual machine with script can be done in two ways.

a. using an inline script.

b. using an external script. 

In this project, we would be using an external script to provision the virtual machine.

To start with, create a file named script.sh in the same location where you have your vagrantfile.

Open the file and paste in the following codes and save.

```
#!/bin/bash

sudo apt update -y
sudo apt install nginx -y
sudo systemctl start nginx
```
![Screenshot 2024-08-11 234047](https://github.com/user-attachments/assets/9b27502e-68fd-415f-8197-1717b96da2a5)

On your vagrantfile, type the code below to configure the shell script.

```
 config.vm.provision "shell", path: "script.sh"
```
![Screenshot 2024-08-18 210758](https://github.com/user-attachments/assets/ed4b698c-c667-4d90-bdb6-e1ba00dafae3)

On your terminal type the code below to provision the machine.

```
vagrant reload --provision
```
![Screenshot 2024-08-12 101208](https://github.com/user-attachments/assets/2fba0988-8d71-4330-82b4-ef5a284d52e3)

Then, type the following code to connect to the guest machine from the host.

```
vagrant ssh
```

Once connected, check for the location of the Nginx and confirm the version with the codes below.

```
which nginx
```
```
nginx -v
```

![Screenshot 2024-08-21 220626](https://github.com/user-attachments/assets/4fae7f13-23d1-412a-8996-a107e471621d)

Logout of the guest machine with

```
Exit
```
### 4. Test the Setup.

Verify that the virtual machine is correctly set up by accessing the Nginx welcome page from your host machine's browser.
On your browser, type http://localhost:8080.


![Screenshot 2024-08-12 100942](https://github.com/user-attachments/assets/60b6bc67-4fc8-4d39-b5d2-c1a73623b9a1)

 Type the code below to check Nginx in the Guest machine too.

```
curl localhost
```
![Screenshot 2024-08-12 101029](https://github.com/user-attachments/assets/c468a391-e06b-4c4c-b559-539ef9632a96)

### 5. Customise the Vagrantfile.

Create a new folder named **app** inside the Devopsenv folder.  

![Screenshot 2024-08-18 205222](https://github.com/user-attachments/assets/ad0a6fd5-0c31-4405-95cd-1972547ed4d0)

Create an index.html file inside your app folder.

![Screenshot 2024-08-18 205302](https://github.com/user-attachments/assets/fa28306e-6037-431e-be07-dd96d0048c99)

In your vagrantfile, Type in the following code to sync the host folder ./app to /var/www/html on the guest.

```
config.vm.synced_folder "./app", "/var/www/html/"
```
![Screenshot 2024-08-18 205554](https://github.com/user-attachments/assets/ba6e845d-75f1-4785-8b1f-75e29dc5a84c)

### 5. Re-provision and Verify.

Type the code ``` vagrant reload --provision ``` in your terminal to re-provision the virtual machine and syncronize the folder.

In your host machine's index.html file, Type ***"Hi buddy, Your Vagrant Environment Setup is Successful!"***

![Screenshot 2024-08-21 235744](https://github.com/user-attachments/assets/5796eb9c-a981-436a-a1a3-a634d1797ff4)

Refresh the browser to access http://localhost:8080 again to verify that it now displays the content of the custom index.html file

![Screenshot 2024-08-21 233835](https://github.com/user-attachments/assets/c01e88bb-5302-4732-92b4-c4c3533499b0)

You can also check the guest machine to confirm that the same thing is displayed on it.

![Screenshot 2024-08-21 234156](https://github.com/user-attachments/assets/76aff5e4-6f79-4b62-a950-7aebe4734793)











