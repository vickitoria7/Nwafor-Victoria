
# SET UP A BASIC SSH HONEYPOT
This project demonstrates the deployment of an SSH honeypot using cowrie to capture and analyze real-world attacker behavior such as brute-force login attempts and command execution.
- Honeypot is a decoy system design as a real venurable target to lure, detect and analyze attackers.
# REQUIREMENTS
* Linux Machine (ubuntu)
* Basic terminal knowledge
# STEP1: UPDATE MY SYSTEM
I started up the my Ubuntu VM which i had already installed, then i open the terminal and bashed in the command to update my system.
               
sudo apt update 

This command doesn't install anything, it only update the list.      
<img width="4032" height="3024" alt="update-system" src="https://github.com/user-attachments/assets/ca4150c7-664e-436f-9590-58f208651b53" />
My system was updated successfully.
# STEP2: INSTALL REQUIRED TOOLS 
The tools i will be using for this project is:
* GIT - This is the tool i will use to dowload code from github, i will use it to get Cowrie.
* PYTHON3 - The Cowrie code is written in python, this will help install the python engine to run it.
* PYTHON3-VENV - This tool will let me create a lightweight virtual environment,like a sandbox that keeps Cowrie's depenendencies separate from my system.
* PYTHON3-PIP - This will let me install python packages, like the previous tools.
* LIBSSL-DEV & LIBFFI-DEV - These are libraries used for encryption, secure connections. cowrie need it to emulate an SSH server, SSH is an encrypted protocol.
* BUILD ESSENTIAL - YES i will be building software,
* -Y - this command will help me automatically say 'yes' to the installation prompts i will give.

   After updating the system, i bashed this command to install the tools i will be using:
  
        sudo apt install git python3 python3-venv python3-pip libssl-dev libffi-dev build-essential -y

   it required my password which i entered and it started installing.
  
  <img width="4032" height="3024" alt="Tools_installation" src="https://github.com/user-attachments/assets/30cae66c-2ddd-49ef-b7b0-e43a274916e2" />
  <img width="4032" height="3024" alt="Tools_Installation2" src="https://github.com/user-attachments/assets/6b9bc6c8-28ce-4c1d-aeb2-2d598a687cc8" />

  All the tools i needed was installed.

  # STEP3: DOWNLOAD COWRIE
  This is the step where i get the cowrie link from github, then in git clone the link by bashing this command:

            git clone http://github.com/cowrie/cowrie.git

This will download all the entire cowrie source code to my system
<img width="3779" height="699" alt="IMG_3425" src="https://github.com/user-attachments/assets/0dfe914b-7c95-43c8-8768-ef36bcd86ede" />
Then i will change into the cowrie directory, this will move me into the cowrie project folder.

      cd cowrie

# STEP4: CREATE A VIRTUAL ENVIRONMENT
This is all about creatimg an isolated python environment, that will prevents conflicts with other python projects and keep my system clean.

     python3 -m venv cowrie-env

* python3 - this will tell my system to run the python3 interpreter.
* -m - this will tell python to run one of my build-in tools, it means run a module as a script.
* venv - this means virtual environment,this is what create isolated environment and keeps dependencies separete.
* cowrie-env - this is just the name of the environment.

Then i activated it, this allows my terminal to works inside that environment.

     source cowrie-env/bin/activate

<img width="3941" height="629" alt="IMG_3423" src="https://github.com/user-attachments/assets/a6c69363-1dde-4918-8752-6c7313e23152" />

# STEP5:INSTALL COWRIE DEPENDENCIES
Inside the activated virtual environment, i installed the required python packages.

     pip install -r --upgrade pip

     











  
