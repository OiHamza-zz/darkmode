Toggle Dark Mode with Touch Bar
====================
Create a Touch Bar shortcut that toggles between dark mode and light mode. 

![cover_image](https://thepracticaldev.s3.amazonaws.com/i/8jkbs2bgnkbf979zs9xu.jpg)

##### This tutorial lives on [dev.to](https://dev.to/oihamza/toggle-dark-mode-with-touch-bar-3o8n)

If you’re anything like me, you enjoy changing between dark mode and light mode based on what vibe you’re feeling.  

Here’s a quick and to-the-point tutorial where I'll show you how to add a shortcut to your MacBook's Touch Bar that makes switching all that much easier. 

🌞🌚 

![cat saying are you ready](https://media.giphy.com/media/CjmvTCZf2U3p09Cn0h/giphy.gif)


What we'll be doing
====================

Very simply, we’ll be creating an Automator script that allows us to create a shortcut for dark/light mode. Once we have the script set up, we will add a Touch Bar shortcut to make switching between the two modes easier. 

If you're not familiar with any of these things, don't worry as I've listed each step with helpful screenshots to guide you. We've got this!

What you’ll need:
====================

- MacBook w/Touch Bar 👆🏽💻
- macOS [Mojave](https://www.apple.com/macos/mojave/)


## Step 1)

<sub><sup>Create the script that automates the light → dark mode process</sup></sub>

→ Open Automater
→ Create a New document
→ Create a quick action, and then click "Choose"

![Create a new document and then quick action](https://thepracticaldev.s3.amazonaws.com/i/y9tfj26coyaci5erppof.png)


## Step 2)

<sub><sup>Implementing the script </sup></sub>

Change the workflow selection to "no input"

![change to no input](https://thepracticaldev.s3.amazonaws.com/i/e8gkxmb7dqy6ulyqlb4g.png)

Change the image to your desired icon. This will appear on the Touch Bar. I selected the color wheel. 

![change the image](https://thepracticaldev.s3.amazonaws.com/i/dd3j2n5smx7ifq16yfl2.png)

In the Actions search bar type "Run AppleScript"

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/kmtyn55qm364sk0xfmqq.png)

Double click "Run AppleScript" and you’ll see this page

![Run AppleScript page](https://thepracticaldev.s3.amazonaws.com/i/db0t33krwu2gqq9k08q9.png)

Delete the existing code, and replace it with the following code:

```
tell application "System Events"
tell appearance preferences 
set dark mode to not dark mode 
end tell
end tell
```
It should look like this:

![Updated code](https://thepracticaldev.s3.amazonaws.com/i/p6z03n4vr7r0fej38sa6.png)

Let's test out the script by clicking the "Run" button

![Test the script](https://thepracticaldev.s3.amazonaws.com/i/9uo887xwl50lzohdn64b.png)

Switch back to the ​light mode by clicking "Run" again. 

Let's go ahead and save the script. I named mine  “Dark Mode Toggle”


![Save your script](https://thepracticaldev.s3.amazonaws.com/i/utqekyfsjy09vfh2wka2.png)

## Step 3)

<sub><sup>Creating the Touch Bar shortcut. We’re almost there!</sup></sub>

On **System Preferences** → **Extensions**, make sure the Dark Mode Toggle is checked

![system preferences → extensions](https://thepracticaldev.s3.amazonaws.com/i/t1b28k86wszx9o53ircs.png)

Click on **Customize Control Strip**

![customize control strip](https://thepracticaldev.s3.amazonaws.com/i/o01a3c1fh339ni7ngcm0.png)

This will take you to this page, where you can drag your quick action to your desired location on the keyboard. I chose to put mine on the far right. 

Note: you'll have to drag it towards the desired place on your Touch Bar. [See more here](https://support.apple.com/guide/mac-help/touch-bar-mchlbfd5b039/mac).

![Touch Bar icons](https://thepracticaldev.s3.amazonaws.com/i/yksx618ds4n3imfxkaec.png)

![Drag the icon to your desired Touch Bar location](https://thepracticaldev.s3.amazonaws.com/i/dxjwra4svarpowwzb9xc.jpeg)


Congratulations, you did it! 😎

Connect with me on Twitter [@oiHamza](https://twitter.com/oihamza). 👨🏽‍🚀
