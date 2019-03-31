# TensorFlow.js Deployment Guide
## Upload a Trained Model
1. Fork this repository
2. Create a new file `mobilenet_1/README.md`
3. Extract `model.zip`
4. Upload all files into `mobilenet_1` folder
5. Click `model.json` > `Raw`
6. Copy raw URL of model.json
7. Download and extract this forked repository
8. Replace the model URL in index.js at tf.loadModel()

## Setup Environment
1. Install Docker
 - Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/
 - macOS: https://docs.docker.com/docker-for-mac/install/
 - Microsoft Windows: https://docs.docker.com/docker-for-windows/install/
2. Pull Docker image (~200MB)
```
docker pull mrteera/tfjs:base
```
3. Run Docker
```
docker run -it --rm -v <tfjs-pacman-full-path>:/root/tfjs-pacman -p 1234:1234 mrteera/tfjs:base /bin/bash
 ```
 For Windows
 ```
 docker run -it --rm -v 'C:\ Downloads\tfjs-pacman:/root/tfjs-pacman' -p 1234:1234 mrteera/tfjs:base /bin/bash
```
4. install TensorFlow.js
```
cd /root/tfjs-pacman
yarn add @tensorflow/tfjs
yarn add @tensorflow/tfjs-node
yarn
```
5. Run `yarn watch`
