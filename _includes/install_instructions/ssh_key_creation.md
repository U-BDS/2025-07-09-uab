---
editor_options: 
  markdown: 
    wrap: 72
---

SSH Token Setup

This is VERY important to do before the workshop in order to complete
the Git workshop. This information can also be found here

1.  Open up your terminal (“git-bash” for Windows or “terminal” for Mac
    and Linux)
2.  To create an SSH key pair use this command, where the `-t` option
    specifies which type of algorithm to use:

```         
$ ssh-keygen -t ed25519
```

2.  The command will ask for a file name, press Enter to use the default

```         
    Generating public/private ed25519 key pair. Enter file in which to
    save the key (/c/Users/Alfredo/.ssh/id_ed25519):
```

3.  You’ll be prompted for a passphrase, be sure to pick something
    memorable as there’s no “reset my password” option. You’ll also note
    you won’t see any of the letters/numbers/symbols you type, this is
    all normal and what you type is recorded even if they don’t show up

```         
Created directory '/c/Users/Alfredo/.ssh'. Enter passphrase (empty for
no passphrase):
```

4.  You’ll be prompted to enter the passphrase again, enter the same
    passphrase you entered in step 3

```         
Enter same passphrase again:
```

5.  After entering the passphrase, you will see something like below.
    (note the specific output will be different for your system, that is
    normal). This means the ssh key is created.

```         
Your identification has been saved in /c/Users/Alfredo/.ssh/id_ed25519
Your public key has been saved in /c/Users/Alfredo/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:SMSPIStNyA00KPxuYu94KpZgRAYjgt9g4BA4kFy3g1o a.linguini@ratatouille.fr
The key's randomart image is:
+--[ED25519 256]--+
|^B== o.          |
|%*=.*.+          |
|+=.E =.+         |
| .=.+.o..        |
|....  . S        |
|.+ o             |
|+ =              |
|.o.o             |
|oo+.             |
+----[SHA256]-----+
```

6.  Run the below command

```         
$ cat ~/.ssh/id_ed25519.pub
```

7.  Copy what is output to the command line, it should look like the
    below:

```         
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIDmRA3d51X0uu9wXek559gfn6UFNF69yZjChyBIU2qKI
```

8.  Go to github.com and login to your account

9.  Click on the profile icon in the top right corner to access the drop
    down menu

10. Click “Settings”

11. Click “SSH and GPG Keys” on the left side, with the “Access” menu

12. Click the “New SSH Key” button

13. Enter a name for the SSH Key (something easy to remember)

14. Paste your key you copied from step 7 into the large text box

15. Click “Add SSH key” to complete setup

16. Go back to the command line, and run this command

```         
$ ssh -T git@github.com
```

17. You should receive output like the below, indicating it a success!

```         
Hi Alfredo! You've successfully authenticated, but GitHub does not provide shell access.
```
