# [OhSINT - Easy][1]
What information can you possibly get with just one photo?

![WindowsXP](/TryHackMe/Challenges/OhSINT/assets/WindowsXP.jpg)

Table of Contents
=================
* [First Steps](#first-steps)
* [Qustion 1: What is this user's avatar of?](#q1-what-is-this-users-avatar-of)
* [Qustion 2: What city is this person in?](#q2-what-city-is-this-person-in)
* [Qustion 3: What is this user's avatar of?](#q3-what-is-the-ssid-of-the-wap-he-connected-to)
* [Qustion 4: What is his personal email address?](#q4-what-is-his-personal-email-address)
* [Qustion 5: What site did you find his email address on?](#q5-what-site-did-you-find-his-email-address-on)
* [Qustion 6: Where has he gone on holiday?](#q6-where-has-he-gone-on-holiday)
* [Qustion 7: What is the person's password?](#q7-what-is-the-persons-password)

### First Steps
First we need to download the task files, we will find that it's a photo of [WindowsXP](/TryHackMe/Challenges/OhSINT/assets/WindowsXP.jpg). so we need obvserve the metadata in the photo using `exiftool`, to install it on Debain based distros run the following command:

```bash
sudo apt install exiftool
```

to retive photo's metadata run this command:

```bash
exiftool WndowsXP.jpg
```

![exiftool](/TryHackMe/Challenges/OhSINT/assets/Exiftool.png)

Under the Copyrights it says the creator name of this image is `OWoodflint`, Let's [Google][2] this name.

![Google](/TryHackMe/Challenges/OhSINT/assets/GoogleSearch.png)

<hr>

### Q1: What is this user's avatar of?
In [Google][2] search results we got a link of [Twitter][3] profile with the same name and a photo of `cat`.

![Twitter](/TryHackMe/Challenges/OhSINT/assets/Twitter.png) <br>

**Answar:** Cat

<hr>

### Q2: What city is this person in?
In the same [Google][2] results we will find [GitHub repositry][4] of `OWoodfl1nt`, and in readme that his location is `London`.

![GitHub](/TryHackMe/Challenges/OhSINT/assets/GithubRepo.png) <br>

**Answar:** London

<hr>

### Q3: What is the SSID of the WAP he connected to?
back to his [Twitter][3] account we will find a [tweet][5] with his BSSID `B4:5D:50:AA:86:41`.

![Tweet](/TryHackMe/Challenges/OhSINT/assets/Tweet.png) <br>

So we'll check [wigle][6] to see if there's a chance to find that WiFi point.

![Wigle](/TryHackMe/Challenges/OhSINT/assets/Wigle.png) <br>

We got a point on the map with SSID `UnileverWiFi`.

![SSID](/TryHackMe/Challenges/OhSINT/assets/SSID.png) <br>

**Answar:** UnileverWiFi

<hr>

### Q4: What is his personal email address?
back to [GitHub][4] we will find his email address is `OWoodflint@gmail.com`.

![GitHub](/TryHackMe/Challenges/OhSINT/assets/GithubRepo.png) <br>

**Answar:** OWoodflint@gmail.com

<hr>

### Q5: What site did you find his email address on?
**Answar:** [GitHub][4]

<hr>

### Q6: Where has he gone on holiday?
In google search results there's a [wordpress][7] site and we will find he is sharing his location `New York`
![Wordpress](/TryHackMe/Challenges/OhSINT/assets/Wordpress.png) <br>

**Answar:** New York

<hr>

### Q7: What is the person's password?
if we inspected the source code of that [site][7] we will find the password `pennYDr0pper.!` hidden .

![Password](/TryHackMe/Challenges/OhSINT/assets/Password.png) <br>

**Answar:** pennYDr0pper.!

[1]: https://tryhackme.com/room/ohsint
[2]: https://www.google.com/search?q=OWoodflint
[3]: https://twitter.com/OWoodflint
[4]: https://github.com/OWoodfl1nt/people_finder
[5]: https://twitter.com/OWoodflint/status/1102220421091463168
[6]: https://wigle.net/
[7]: https://oliverwoodflint.wordpress.com/author/owoodflint/