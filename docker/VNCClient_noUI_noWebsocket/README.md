# [EDGE APP] VNC Client for Unified Panels
## Hardcoded connection parameters
Included docker-compose file allows you to build specific version of the app, that supports the VNC servers **not supporting** websocket mechanisms, e.g. Windows based servers. However, the connection parameters are hardcoded and it is not possible to change them without rebuilding the app.

## Installation
1. Use Industrial Edge App Publisher to build the Edge app based on included **docker-compose.yaml** file. Instructions how to build the Edge app can be found in the [documentation](https://docs.eu1.edge.siemens.cloud/develop_an_application/ieap/preface.html).