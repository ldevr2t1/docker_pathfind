# Generic Server Image
### How-to
1. go ahead and gitclone this repo
`git clone https://github.com/ldevr2t1/docker_pathfind.git'
2. navigate into the web directory (i.e. cd web)
3. run docker commands to get server running
`docker-compose build`
`docker-compose run`

#### NOTE
This is under the assumption you have docker installed.

### To configure host/ui address
If you want to change the server's IP-address edit the 'host' parameter in main
`web/swagger_server/__main__.py` 
Also change the host parameter in the swagger.yaml file for the UI to work
`web/swagger_server/server/swagger.yaml`


### Changing the port number
1. Change the port in the same files for configuring the host/ui address
2. Go into the base directory /docker_pathfind and edit the docker-compose.yml
`Change the Ports configuration to the ports you desire`
