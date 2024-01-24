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
5. Select file from the panel storage (eg. external USB device) or browse your computer files, depending on where you have opened the Management.
6. Skip the configuration tab and install the file.
7. Go to Management tab and Start the application (it does not start automatically).

## Connecting with Sm@rt Server
### Requirements
- Sm@rt Server is enabled and configured on target device.
- TLS encryption is disabled (option **Secure communication via self-signed certificate** is unticked in Sm@rt Server settings).
  
> [!CAUTION]
> Current version of the application does not support encrypted connection. Client can be used for connecting with other VNC servers but they have to support websocket connection mechanism!

> [!IMPORTANT]
> Client can be used for connecting with other VNC servers but they **have to support websocket** connection mechanism! The app has been tested with Sm@rt Server on HMI Unified Panels and VNC servers running on Linux machines. Tests performed with classic Comfort panels and Windows based, popular VNC servers (like TightVNC) were not successful due to lack of support for websockets mechanism.

### Extablishing connection
1. Open app on your panel by clicking the proper tile in your Edge Management.
2. Enter connection data - address of your Sm@rt Server and port number (default port is 5900, you can change it in Sm@rt Server settings) and click **Connect** button.
3. If the server is accessible in you network and connection data was correct, you will be prompted for access password.

