Server Image
### How-to
1. go ahead and gitclone this repo
`git clone https://github.com/ldevr2t1/docker_pathfind.git`
2. navigate into the web directory (i.e. cd web)
3. run docker commands to get server running
    * `docker-compose build`
    * `docker-compose run`

### To configure host/ui address
1. To change the server's IP-address edit the **'host'** parameter in main.
    * `File: web/swagger_server/__main__.py`
        - `app.run(host='<your_address>', port=<port_number>)`
    
2. Change the host parameter in the **swagger.yaml** file for the UI to work
    * `web/swagger_server/server/swagger.yaml`
        - `host: "<your_address>:<port_number>"`

### Changing the port number
1. Change the *<port_number>* in the same files for configuring the host/ui address
2. Go into the base directory /docker_pathfind and edit the **docker-compose.yml**
    * `ports: ` 
        `- "<port_number>:<port_number>"`
3. Change the **Dockerfile** (i.e. change the EXPOSE #)
    * `#Expose port # for testing`
    -`    EXPOSE <port_number>`


#### NOTE
This is under the assumption you have docker installed.
