## SSH Tunnel for Android OS


### Summary:
In this tutorial you are going to learn how to use ssh tunel to make your own vpn.    

<br>

### Requirements:

1. termux
2. matsuri

<br>

### Step 1 - Creating new SSH
Go to website [vpnjantit.com](https://vpanjantit.com)
1. Click on Free VPN SSH
2. Create Free SSH Tunnel
3. Choose a Country (France & Italy suggested)
4. Set username and password (set both the same)
5. Check the checkbox of "I'm not a robot"
6. Click on Create Free SSH Tunnel
7. Click on Show IP from the right side of the page
8. Copy the given IP.
done

<br>

### Step 2 - Install the Termux requirements
Open Termux and run these commands:

```text
    pkg install dropbear
```

After installing dropbear install openssh

```text
    pkg install openssh
```

After installing openssh run this command to connect the SSH:

```text
    ssh -p 22 -N -D 4002 username-vpnjantit.com@IP
```
After that, if termux wants to set fingerprint, type "yes" then you need to put your password:

The Termux must do nothing else.

<hr>

### Step 3 - Install the Matsuri proxy

<br>

#### 1. Create new proxy in matsuri
   1. Touch on import
      1. Manual settings and set these configurations:
         - Choose SOCKS5 type
         - Set a name for your proxy
         - Server: 127.0.0.1
         - Remote port: 4002
         - Save the proxy

<br>

#### 2. Route Settings:
   1. Touch on 3line at the left top corner of the app
        1. Touch on "Settings"
           1. In settings bar find Route Settings section
                1. Set "Apps VPN mode" On & Touch on it:
                    - Set the option on "proxy"
                    - Choose each app you want to use ssh on it
                    

Now you can run the proxy and enjoy the free internet.

---
### Note: 
    Each time you want to use this first run the SSH on "Termux" then Start your "proxy"

