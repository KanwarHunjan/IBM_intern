

# Hyperledger Fabric

Hyperledger Fabric is a blockchain framework implementation and one of the Hyperledger projects hosted by The Linux Foundation. Intended as a foundation for developing applications or solutions with a modular architecture, Hyperledger Fabric allows components, such as consensus and membership services, to be plug-and-play. Hyperledger Fabric leverages container technology to host smart contracts called “chaincode” that comprise the application logic of the system.
In this document you will be getting a step by step guide on how to make a multi peer network in the fabric on a windows platform specifically.

1.**Instal Docker**:
Docker version 17.06.2-ce or greater is required, for Older versions of Windows: Docker Toolbox - again, Docker version Docker 17.06.2-ce or greater is required. You can easily download it from the official site of the docker community.
You can check the version of Docker you have installed with the following command from a terminal prompt:
docker --version

Before running any git clone commands, run the following commands:
- git config --global core.autocrlf false
- git config --global core.longpaths true

You can check the setting of these parameters with the following commands:
- git config --get core.autocrlf
- git config --get core.longpaths

2.**Instal Nodejs**:
You have to install nodejs for some commands to work, you can download it from the official nodejs site. This should be done in the windows power shell(Administrative mode).
we can install it using the following command in windows power shell:
- npm install --global windows-build-tools

The above step should be done in the windows power shell(Administrative mode) , followed by another command:-
- npm install --global grpc

3.**Determine a location**:
If you are using Docker Toolbox on Windows 7 or macOS, you will need to use a location under C:\Users (Windows 7) or /Users (macOS) when installing and running the samples.
Determine a location on your machine where you want to place the Hyperledger Fabric samples applications repository and open that in a terminal window. Then, execute the following commands:
- git clone -b master https://github.com/hyperledger/fabric-samples.git
- cd fabric-samples

4.**Instal platform-specific binaries**:
Next, we will install the Hyperledger Fabric platform-specific binaries. This process was designed to complement the Hyperledger Fabric Samples above, but can be used independently. If you are not installing the samples above, then simply create and enter a directory into which to extract the contents of the platform-specific binaries.
Please execute the following command from within the directory into which you will extract the platform-specific binaries:-

- curl -sSL https://goo.gl/6wtTN5 | bash -s 1.1.0

5.**Export Path**:
You may want to add that to your PATH environment variable so that these can be picked up without fully qualifying the path to each binary. e.g.:
- export PATH=<path to download location>/bin:$PATH
- export PATH=/C:/Users/Khushal/exp/fabric-samples/bin:$PATH
Finally, the script will download the Hyperledger Fabric docker images from Docker Hub into your local Docker registry.

6.**Build your first network**:
The build your first network (BYFN) scenario provisions a sample Hyperledger Fabric network consisting of two organizations, each maintaining two peer nodes, and a “solo” ordering service.
You will also need to download and install the Hyperledger Fabric Samples. You will notice that there are a number of samples included in the fabric-samples repository. We will be using the first-network sample. Let’s open that sub-directory now.
- cd fabric-samples/first-network

**Generate required certificates**
- ./byfn.sh -m generate

**Bring Up the Network**
- ./byfn.sh -m up

**Bring Down the Network**
- ./byfn.sh -m down

Hence this documentation shows the easy installation and working of a multi peer hyperledger fabric on windows platform. 
