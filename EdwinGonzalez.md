## CST 8254 Practical Mid Term

**Your Name:**

```
Edwin Gonzalez Mendoza
```

Answer directly in this .md file.

### Task 1:

1. Connect to your raspberry pi through SSH
2. Start a terminal session then type `sudo raspi-config` . Navigate the various menu options to

   - make sure VNC are enabled.

### Task 2:

On your pi, issue the following commands one by one in sequence

```
hostname -I
df
pwd
date
```

Take a screenshot **start.jpg**, and upload the jpg file to GitHub **NOW**.

On your pi, issue the following commands

```
cd /var/www
ls
```

Take a screenshot **start1jpg**, and upload the jpg file to GitHub **NOW**.

On your laptop, in any folder, create a text file whose name is the concatenation of your firstname and your lastname . For example mine would read **`jeromemizon.txt`**. Open the file and add a line saying that you were there. For instance mine would read: **`Jerome Mizon was there.`**

Make sure your Pi is connected on your home network.

Using `scp` , send a copy of the file to your raspberry pi in the home folder. **What command did you use?**

**1.**

```
scp Edwin_Gonzalez.txt pi@192.168.4.247:/home/pi/
```

Open a **`putty/ssh`** session to your raspberry pi .

**2. What command do you use to see a directory listing that includes the permissions of the files?**

```
ls -l
```

Redo the last command and save the output of the command to a file **`pr1.txt`**. **What command did you use?**

**3.**

```
ls -l > pr1.txt
```

**4. What are the permissions of the file you just created?**

```
-rwx--x--- 1 pi pi 32 Jun 18 11:34 edwingonzalez.txt

```

**5. What command do you use to display the folder you are currently working from?**

```
pwd
```

Change the permissions of the file so that group members can only execute it. **What command did you use?**

**6.**

```
chmod 710 Edwin_Gonzalez.txt
```

Create a folder **`midtermExam-SectionNumber`** under the current working directory of your raspberry pi. **SectionNumber** must be replaced with your lab section number (for instance Jérôme's Lab students use 301). **What command did you use?**

**7.**

```
mkdir midtermExam-301
```

**8. What are the permissions of this new folder ?**

```
drwxr-xr-x 2 pi pi 4096 Jun 18 11:40 midtermExam-301

```

**9. What command do you use to list the ports your raspberry pi is listening to? Try it using the `-at` flag.**

```
netstat -at
```

Redo the last command saving the output of the command to a file **`pr2.txt `**. **What command did you use?**

**10.**

```
netstat -at > pr2.txt
```

On your laptop create a text file **`midtermPi.txt`**. The content of the file is a line stating that you were there. For instance mine would read: `**Jerome Mizon was there.**` Save the file.

From the command line start a sFTP session to your raspberry PI . **What command did you use to connect?**

**11.**

```
sftp pi@192.168.4.247
```

Copy the file **`midtermPi.txt`** to your PI using sFtp. **What command did you use?**

**12.**

```
put midtermPi.txt
```

On your PI run the following command

```
pwd>mt.txt;tree -l>>pr.txt
```

**13.** What does the command do?

```
1- Saves your current folder path into mt.txt.

2- Then, appends the visual folder structure of the current directory to pr.txt.

```

Using `useradd`, create a user named after you using the concatenation of your firstname and last name. **What command did you use?**

**14.**

```
sudo useradd egonzalez
```

Create the home directory for the user you just created and change the ownership of this folder to the user himself/herself. **What commands did you use?**

**15.**

```
sudo mkdir /home/egonzalez
sudo chown egonzalez:egonzalez /home/egonzalez
```

Update your PI package list using `apt-get` , then use `apt-get` to install `Filezilla` on your PI. **What commands did you use?**

**16.**

```
sudo apt-get update
sudo apt-get install filezilla -y
```

**17.** issue the following command on your pi:

`cd /home`

`ls -als > /home/pi/pr3.txt`

### Task 3:

Install the following packages on your Pi using `apt-get`. Install them in the following order

1. Apache2: `sudo apt-get install apache2 -y`

2. Mariadb: `sudo apt-get install mariadb-server`

   Once installed, issue the following commands one by one from a terminal/command prompt window. Make sure you replace 'password' with a password of your choice.

   ```
   sudo mysql

   CREATE USER 'pi'@'localhost' IDENTIFIED BY 'password';

   GRANT ALL PRIVILEGES ON * . * TO 'pi'@'localhost';

   FLUSH privileges;

   EXIT;
   sudo service mysql restart
   ```

3. Php: `sudo apt-get install php`

4. Phpmyadmin: `sudo apt-get install phpmyadmin`
   Install it on the pi Apache web server.

From your laptop, connect to the pi phpmyadmin site using the ip address of your pi. Make a screenshot and name the screenshot `phpmyadmin.jpg`. Note that the screenshot must show the address bar of your browser.

### Task 4:

Intall a copy of Wordpress on your Pi.

The following site will assist you:

https://projects.raspberrypi.org/en/projects/lamp-web-server-with-wordpress/5

When setting up the wordpress database, log on using the user you created instead of using the`root` user as specified.

Install wordpress.

From your laptop, connect to the pi wordpress site using the ip address of your pi. Log on the wordpress site. Make a screenshot and name the screenshot `wpress.jpg`. Note that the screenshot must show the address bar of your browser.

### Final Steps:

On your PI run the following commands

```
cd ~
ls -l > pr4.txt
cat /etc/passwd | tail -n2 > pr5.txt
```

On your pi, issue the following commands one by one in sequence

```
hostname -I
df
pwd
date
```

Take a screenshot **end.jpg**, and upload the jpg file to GitHub **NOW**.

---

Using `sftp` or `Filezilla`, transfer the files **`pr.txt,pr1.txt,pr2.txt,pr3.txt,pr4.txt,pr5.txt` to your laptop then upload them to GitHub. No Zip file, only text files, \*\*\*\***zip files will not be graded**.**

**Upload the two jpg files wpress.jpg and phpmyadmin.jpg to GitHub.**

---

**Edit this md file to only include the questions numbers and your answers as in .**

**1.**

```

```

**2. What command do you use to see a directory listing that includes the permissions of the files?**

```
ls -l
```

1.  scp edwingonzalez.txt pi@192.168.1.10:/home/pi/

2.  ls -l

3.  ls -l > pr1.txt

4.  -rwx--x--- 1 pi pi 32 Jun 18 11:34 Edwin_Gonzalez.txt

5.  pwd

6.  chmod 710 Edwin_Gonzalez.txt

7.  mkdir midtermExam-301

8.  drwxr-xr-x 2 pi pi 4096 Jun 18 11:40 midtermExam-301

9.  netstat -at

10. netstat -at > pr2.txt

11. sftp pi@192.168.4.247

12. put midtermPi.txt

13. pwd > mt.txt; tree -l >> pr.txt

14. sudo useradd egonzalez

15. sudo mkdir /home/edwingonzalez
    sudo chown egonzalez:egonzalez /home/egonzalez

16. sudo apt-get update
    sudo apt-get install filezilla -y

17. cd /home
    ls -als > /home/pi/pr3.txt
