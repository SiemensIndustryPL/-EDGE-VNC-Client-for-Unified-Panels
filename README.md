# [EDGE APP] VNC Client for Unified Panels
Simple Edge application working as VNC client for connecting with Sm@rt Server by means of Unified Comfort panels.

## Requirements
- HMI Unified Comfort panel
- Valid Edge License for Unified Comfort panels (6AV2170-2BA00-0AA0)

## Installation
1. [Download compiled .app file](https://github.com/SiemensIndustryPL/-EDGE-VNC-Client-for-Unified-Panels/raw/main/VNCClient_ForUnifiedPanels.app?download=) from this repository using web browser or execute command `git clone https://github.com/SiemensIndustryPL/-EDGE-VNC-Client-for-Unified-Panels.git` if you have Git installed on your computer.
2. Go to **Apps -> SIMATIC Edge -> Open edge management** section on the panel or type the panel IP address in web browser to open the Edge Management on your computer.
3. Log into your Edge Management using login and password configured in the WinCC project.
4. Click **Install Offline** button which can be found in the top right corner oy the Edge Management.
   
   ![Install offline button from Edge Management](https://github.com/SiemensIndustryPL/-EDGE-VNC-Client-for-Unified-Panels/blob/main/src/installbutton.png)
6. Select file from the panel storage (eg. external USB device) or browse your computer files, depending on where you have opened the Management.
7. Skip the configuration tab and install the file.

## Connecting with Sm@rt Server
### Requirements
- Sm@rt Server is enabled and configured on target device.
- TLS encryption is disabled (option **Secure communication via self-signed certificate** is unticked in Sm@rt Server settings).
  
> [!CAUTION]
> Current version of the application does not support encrypted connection.

### Extablishing connection
1. Open app on your panel by clicking the proper tile in your Edge Management.
   
   ![Application tile in Edge Management](https://github.com/SiemensIndustryPL/-EDGE-VNC-Client-for-Unified-Panels/blob/main/src/apptile.png)
3. Enter connection data - address of your Sm@rt Server and port number (default port is 5900, you can change it in Sm@rt Server settings) and click **Connect** button.
   
   ![Connection window](https://github.com/SiemensIndustryPL/-EDGE-VNC-Client-for-Unified-Panels/blob/main/src/connectionwindow.png)
5. If the server is accessible in you network and connection data was correct, you will be prompted for password. If the password is correct, you should have access to the runtime and panel OS.

### Credits
Main core of the application is noVNC Library distributed under MPL 2.0 license. You can find it here: [noVNC on GitHub](https://github.com/novnc/noVNC)

