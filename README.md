
## 3DScan Enabler Installation and Execution

This section describes the necessary steps to install the prepared/validated enablers. The selected enablers are provided with a Dockerfile and a docker-compose if necessary.

### Requirements
To install and execute the enabler it is necessary to have a Docker environment installed. 
More information can be found at https://docs.docker.com/get-started/

### Installation
To install the enabler, it is necessary to create the image from the Dockerfile. 
To do it type the following command on bash, at Dockerfile location by performing the command below. 
Start first with the 3DScan database, and second with the 3DScan Enabler (which needs to connect to database when deploying). 

#### 3DScan Mysql Database : 

```
Docker build .
```

Then execute this command to start the deployment of the image

```
docker run -it --rm  -p 3306:3306 mysql3dscan
```

#### 3D Scan Enabler 

```
Docker build .
```
Then execute this command to start the deployment of the image

```
docker run -it --rm  -p 8080:8080 3dscan
```

### Execution

To run the enabler from the previously created image perform:

```
docker run -it --rm  -p 3306:3306 mysql3dscan
```

```
docker run -it --rm  -p 8080:8080 3dscan
```
