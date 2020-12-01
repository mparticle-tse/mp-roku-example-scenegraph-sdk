<img src="https://static.mparticle.com/sdk/mp_logo_black.svg" width="280">

# mp-roku-example-scenegraph-sdk

This is a example app that is mainly derived from the example in the [MP Roku SDK](https://github.com/mParticle/mparticle-roku-sdk). 

The Main differences are that this sample only contains the Scenegraph SDK as the [Legacy SDK is no longer supported](https://blog.roku.com/developer/2017/02/01/legacy-sdk) and that this one contains a ```launch.json``` file in the ```.vscode``` directory that is used in conjunction with the [Brightscript plugin for VSCode](https://marketplace.visualstudio.com/items?itemName=RokuCommunity.brightscript) to run a debugger. 

# Getting Started 

**You will need a Roku Device to use this sample properly**

Follow the instructions provided to you in the box that your Roku came with or if they were missing use this guide from [their site](https://support.roku.com/article/208754888).

If you are not seeing anything on your screen but hear audio feedback when clicking the buttons on the remote, try switching to another input on your TV then switching back to the input your Roku is on. 

Once your Roku is connected, you will now have to enable developer settings and navigate to the Development Application Installer 
[Roku offers a great guide on how to do this](https://developer.roku.com/docs/developer-program/getting-started/developer-setup.md). 

If you are finding that you are unable to connect to your Development Application Installer make sure you are on the same WiFi / Connection as your Roku device. For example, if you installed your Roku and it is connected to your home Wifi and you are on the VPN, you will not be able to connect to your Roku’s URL. 

Once you are able to access Development Application Installer screen you will want to create a sample channel to make sure everything is setup correctly
The Application Installer page only accepts a channel contained in a ZIP file. This process is called "sideloading" your channel. 
Roku provides a “hello world” ZIP file and a [Hello World guide](https://developer.roku.com/docs/developer-program/getting-started/hello-world.md) on how to install and run the sample channel on your Device. Once this is running you are good to move to the next step

# Setup mParticle example-scenegraph-sdk

git clone the repo and cd into the example-scenegraph-sdk directory. 

Navigate to the Main.brs file in the Source folder and update the API Key and Secret with the ones you created in the mParticle platform for the Roku input. 
In the same Source folder go to the mParticle folder and do the same in the mParticleCore.brs file.

In the Main.brs file make sure to comment out the options.dataPlanId = "REPLACE WITH DATA PLAN ID" line if you are not using a data plan. 

cd into the Source folder in the terminal and run “make” this will create a dist/ directory that contains the ZIP file you will upload to the Development Application Installer

Once you upload your ZIP file to the Development Application Installer and click Install / Replace you should see your Roku change to your channel. 

# Using the VSCode Brightscript Plugin / Debugger

The Brightscript Plugin for VSCode is very very helpful tool for testing with Roku. By using the debugger instead of sideloading your channel each time you will save an enormous amount of time. **This is the best way to test**. 


The guide linked [here](https://marketplace.visualstudio.com/items?itemName=RokuCommunity.brightscript) explains how to install the plugin and setup the ```launch.json``` file needed to run the debugger. I have already included the file in the repo. All that is needed is to install the plugin and update the Host and Root Directory. You should then be able to run the Debugger and see events in the LS and console. 







