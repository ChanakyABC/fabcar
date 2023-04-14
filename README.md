# README


## Prerequisites

### 1. Hyperledger Fabric Setup Installation guide on Ubuntu
[Hyperledger Fabric Setup Guide](https://docs.google.com/document/d/1lzuE5PiHIlOaTt2r2b-lXiug1euvBgzpnzFkRbyPYrk/edit?usp=sharing)

### 2. Clone the FABCAR repo from the given link :
https://github.com/ChanakyABC/fabcar.git




## Getting started with Fabric

1. Open terminal or any file explorer and go to the fabcar folder.
```bash
cd fabcar
```

2. Shut down any previously running networks on fabric.
```bash
./networkDown.sh
```


3. Remove any previously created docker containers.
```bash
docker rm -f $(docker ps -aq)
```

4. Prune the network if any before setting up the network.
```bash
docker network prune
```

5. Install all the dependencies.
```bash
npm install
```

6. Run the fabric script file startFabric.sh
```bash
./startFabric.sh
```

7. Before interacting with the fabric, we need an Admin and user credentials.
Creating Admin certificates  
```bash
node enrollAdmin.js
```
8. Creating User certificates
```bash
node registerUser.js
```

9. Run the query file to interact with the fabric using chaincode and make a get request to the fabric.
```bash
node query.js
```

10. Run the invoke file to interact with the fabric using chaincode and make a Post or Update request to the fabric.
```bash
node invoke.js
```

