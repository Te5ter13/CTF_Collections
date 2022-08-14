## CTF
link: https://sankalpa1337.netlify.app/

**First page Info**

Give me the flag !!
****TOP SECRET ACCESS****
Accessing Server Identity
Server Name:....................
Anonymous

User: S4NK41P4
Naviagate to /.......html (You should not trust me)
So you are here to find the flag?
Good luck
-S4NK41P4 

# Time to search for the directory
gobuster:
/index                (Status: 301) [Size: 969] [--> /]
/Index                (Status: 301) [Size: 969] [--> /]
/index.htm            (Status: 301) [Size: 969] [--> /]
/index.html           (Status: 200) [Size: 969]
/robots.txt           (Status: 200) [Size: 202]
/secret               (Status: 200) [Size: 9281]


*First wordlist: robots.txt*

# at /robots.txt

Hello Ben, thanks for teaching me about EXIF data now whenever I see a image I try to check if there's any EXIF data or not
Another important thing I encoded your password to >>  YmVuYmVuYmVu
 YmVuYmVuYmVu --> base64-decode --> benbenben

# found the image at /index
at script.js file there's download.png and redirecting to home page adding download.png get the image of robot.

# using the Exiftool for the image
got the link:
https://www.mediafire.com/file/k5bsst6hit3sbgg/Ben.zip/file

# Found Ben.zip file 
extract with benbenben password(cracked password) using cmd:
7z x Ben.zip

*got the .......txt file* 
it contains text as:
464c41477b6b397a4a4c614f66717457456479426c497171576e5076754861357434447d

*After searching i found it tends to be encoded hexdump file, so to decode it*

echo "464c41477b6b397a4a4c614f66717457456479426c497171576e5076754861357434447d" | xxd -p -r
and got the flag
FLAG{k9zJLaOfqtWEdyBlIqqWnPvuHa5t4D}

