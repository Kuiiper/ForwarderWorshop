# Workshop Overview
Today's workshop will cover the basics over setting up a Splunk Universal Forwarder and connecting it to an active Splunk server. You will need VPN access, and any available machine you are willing to install the Splunk Forwarder on. If you are using your personal laptop. please remember to delete the Forwarder after the workshop.

## Steps
In this workshop you will need to:
1. Download and install the forwarder
2. Configure the forwarder with the appropriate information
3. Make associated host changes to allow communication
4. Verify that your forwarder is communicating with the Splunk Server

## 1. Download and Install
For this section you will need to gather the download thing. Normally, this is done by accessing the Splunk website and finding the appropriate URL for your operating system. For the sake of speed, we will provide you with the URLs you will need:
### Windows

[https://download.splunk.com/products/universalforwarder/releases/9.4.0/windows/splunkforwarder-9.4.0-6b4ebe426ca6-windows-x64.msi](https://download.splunk.com/products/universalforwarder/releases/9.4.0/windows/splunkforwarder-9.4.0-6b4ebe426ca6-windows-x64.msi)

### Linux Debian/Ubuntu
```
wget -O splunkforwarder-9.4.0-6b4ebe426ca6-linux-amd64.deb "https://download.splunk.com/products/universalforwarder/releases/9.4.0/linux/splunkforwarder-9.4.0-6b4ebe426ca6-linux-amd64.deb"
```
Once downloaded, you should be asking yourself "What exactly did I download". As in, is the app you downloaded actually ready to be used or do you need to install first? If so, how do you do that according to the operating system you are using? What package manager? etc.

## 2. Configure Forwarder
Now that the forwarder has been downloaded and installed, you will need to configure the application.
### WIndows
For Windows, all of the configurations can be done using the bootstrapper for the application. This process is straightforward, and all of the information you will need is provided at the top of the workshop or on the presentation screen.
### Linux
Linux will require a more advanced command of the Linux terminal, you will need to find out how to pass the proper arguments to the application using the command line. You will need to add a Deployment server and a Log Reciever, at this moment, it would be advised to visit the official Splunk documentation to find out how to do this.

## 3. Make Host Changes
With the previous steps complete, you may not immediately see your forwarder on the Splunk server, and this could be for a multitude of reason. But before you reinstall, think about what is necessary for your forwarder to communicate to the Splunk Server. What types of traffic will need to be exchanged between client and server, and what can you do to allow that flow?
## 4. Verify
The Splunk Server should be displayed on the board with a list of forwarders that have connected. The page will be refreshed periodically, and you can request that the page be refreshed. Once the forwarder appears in the list, it would be advised to check the logs to see if the forwarder has produced any, if not, then the process might not be fully complete.
