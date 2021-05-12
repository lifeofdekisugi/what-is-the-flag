# what-is-the-flag
# What is the flag - Walkthrough


[Click here to download the challenge file](https://mega.nz/file/XkpxDSBZ#eeO-8PcAKyT4kSrCubYtIqkpiPzGsteK8DODyd8nC6Y)

After downloading you will see a file named **unzip_it.zip**

It's password protected you need to bruteforce it. I use fcrackzip

```
fcrackzip -u -D -p /usr/share/wordlists/rockyou.txt unzip_it.zip

passwd is : tequila27

```

After unzipping the file you will see a image called **hello_hacker.jpg**

If you **steghide** it then it will need a password to extract data.

Then you can use **stegcracker** to bruteforce the image file to get password. After bruteforce you will see the password and it will automatically create a file named **hello_hacker.jpg.out** this file will have everything you need.

```
Ok So you are here,

  First part of the flag : ictf{y0u_

  Check the link for next step

  https://jpst.it/2vlhr

```

Now we have first part of the flag **ictf{y0u_** and a link. If you visit the link then you can see a lot of garbage there but no they are not garbage that is **Brain Fuck Encoding.** Now you need to [decode](https://www.splitbrain.org/_static/ook/) it.

After decoding you can see

```
Wow, that's dope man ! You are doing good.
It's time for second part of the flag and here it is : g0t_

Probably I can belive you so, Let me share my location with you. Please don't share with anyone because CIA finding me. My BSSID : B4:5D:50:AA:86:41

Check this link to get third part of the flag.
https://jpst.it/2vlgO

```

We have another link and second part of the flag **g0t_**. In this link you have Vigenere Encode if you want to decode it then you need a key. The decoding key is my WIFI **SSID.** You can see in the previous part I shared my **BSSID.**

If you want to get SSID of that BSSID then you can find it on [WIGLE](https://wigle.net/) (Probably you need to sign in).

After getting the SSID you can use that **UniliverWifi** as  Vigenere decoding key. After decoding you can see

```
Wow, nice ! Crack the last part and anjoy.

Nice dude !!! Here is the third part : last_

Next Otep : https://justpaste.it/8n01k

```


Ahh gosh !! We have another link and third part of the flag **last_**. Here we have Morse Code let's [Decode it](https://morsedecoder.com/)

```
SO YOU ARE HERE. YOU ARE MY FAVOITE ONE FROM THE SERVER
HERE IS YOUR LAST PART OF THE FLAG : PART_OF_FLAG#


```

Here we have

And here we have our last part of the flag : **part_of_flag}**

# Full flag : ictf{y0u_g0t_last_part_of_flag}

Thank You
