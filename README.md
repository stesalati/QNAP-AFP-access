# QNAP-AFP-access
How to access files in a QNAP NAS remotely from a MacBook.

Tested on QNAP TS-453A.

# Steps
## Installation of Debian in a container and basic configuration
Create Debian container on the NAS with ContainerStation.
![Alt text](readme1.jpg)

Share the folders you want to access
![Alt text](readme2.jpg)

At this point you should be able to work in the console.

Make that usable by refreshing packages and make installing packages possible:
```
apt-get update
apt-get upgrade
apt-get install wget
apt-get install ssh
```

Set root password (not sure if this can be skipped)
`passwd`

Create new non-root user. Authentication to root did not work even with the right configuration. See https://superuser.com/questions/543626/ssh-permission-denied-on-correct-password-authentication and https://chiedi.ubuntu-it.org/questions/52866/accesso-negato-ssh-permission-denied-publickeypassword in case of problems.
`adduser ste`

Download and install the right version of Hamachi from: https://vpn.net/linux.
```
wget https://vpn.net/installers/logmein-hamachi_2.1.0.203-1_amd64.deb
dpkg -i logmein-hamachi_2.1.0.203-1_amd64.deb
```

4. Configure Hamachi by logging in and joining the right virtual LAN: https://support.logmeininc.com/central/help/how-to-attach-an-unattached-client-to-a-logmein-account-central-t-hamachi-add-attachexisting

5. Install Hamachi on the MacBook anbd configure it. At this point the Debian in the container should show up in the hamachi window on the MacBook.


7. 

9. At this point you should be able to ssh to it
10. Install opensource implementation of AFP:
    1. https://mycyberuniverse.com/linux/afp-and-bonjour-under-linux.html
    2. apt-get install netatalk
    3. nano /etc/default/netatalk
11. D
12. D
13. dadducer
