# [OhSINT - Easy][1]
What information can you possibly get with just one photo?

After downloading the task files, we will find that it's a photo of WindowsXP.so we need obvserve the metadata in the photo using `exiftool`, to install it on Debain based distros run the following command:

```bash
sudo apt install exiftool
```

to retive photo's metadata run this command:

```bash
exiftool WndowsXP.jpg
```

Under the Copyrights it says the creator name of this image is `OWoodflint`, Let's Google this name.

google photo
### Q1: What is this user's avatar of?
In Google search results we got a link of Twitter profile with the same name and a photo of `cat` <br>
twitter photo
**Answar:** Cat

### Q2: What city is this person in?
In the same Google results we will find GitHub repositry of `OWoodfl1nt`, and in readme that his location is `London`
Repo photo
**Answar:** London

### Q3: What is the SSID of the WAP he connected to?
back to his Twitter account we will find a tweet with his BSSID `B4:5D:50:AA:86:41`
tweet photo
So we'll check wigle.com to see if there's a chance to find that WiFi point
Wigle photo

We got a point on the map with SSID `UnileverWiFi`
point photo 
**Answar:** UnileverWiFi

### Q4: What is his personal email address?
back to GitHub we will find his email address is `OWoodflint@gmail.com`
github photo
**Answar:** OWoodflint@gmail.com

### Q5: What site did you find his email address on?
**Answar:** GitHub

### Q6: Where has he gone on holiday?
In google search results there's a wordpress site and we will find he is sharing his location `New York`

### Q7: What is the person's password?
if we inspected the source code of that site we will find a white hidden text with the password.
password photo

[1]: https://tryhackme.com/room/ohsint