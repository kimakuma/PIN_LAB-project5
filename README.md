![header](https://capsule-render.vercel.app/api?type=soft&color=006EDB&fontColor=DEEAF7&height=200&section=header&text=PIN_LAB&desc=Project%205&descAlignY=80&fontSize=90)
# PIN_LAB: Project 5

Text conversion of WAV file using Google Cloud Platform's Speech-to-Text API

---

## Navigation
1. [Description](#Description)
2. [Getting started](#Getting-Started)
3. [Architecture](#Architecture)

---

## Description
Text conversion of WAV file using Google Cloud Platform's Speech-to-Text API on Raspberry PI 400
- Recording WAV file
    - [WAV file description](https://crystalcube.co.kr/123)
- Using GCP STT API to convert WAV file to Text
- Saving WAV file with meta datas including converted text via Atlas(MongoDB)

---

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 
See deployment for notes on how to deploy the project on a live system.

### Installing & Setting (based on Code)
- Installing the pip
    - pip: for Python 2.x
    - pip3: for Python 3.x
```console
sudo apt-get install python-pip3
```

- Installing the [PyMongo](https://kb.objectrocket.com/mongo-db/how-to-install-pymongo-and-connect-to-mongodb-in-python-363)
```console
pip3 install pymongo
```

- More packate to install are in Dockerfile

- More examples for [Python-sounddevice](https://python-sounddevice.readthedocs.io/en/0.4.1/examples.html#play-a-sound-file)

- Setting Sound device
```console
python3 -m sounddevice
```

### Installing & Setting (based on Docker)
- docker: [kimakuma8/ubuntu:project5](https://hub.docker.com/layers/kimakuma8/ubuntu/project5/images/sha256-8cf20343f696e5d59252f7b1ac4414f1cafd52551e400b9856be05765a131702?context=repo)

- Grant sound device permission in Docker
```console
sudo isermod -aG docker $USER
sudo su - $USER
docker run --device /dev/snd/ -it { Docker image }
```

- Installing [PortAudio](http://files.portaudio.com/docs/v19-doxydocs/compile_linux.html)
```console
sudo apt-get install libportaudio2
```

---

## Architecture
### Docker
<img src="https://user-images.githubusercontent.com/76460405/204084157-f98f2178-5799-4da2-88bd-6eb2d32da4bf.png" width="590" height="214">

### Architecture
<img src="https://user-images.githubusercontent.com/76460405/204084264-f78f6e4c-fe85-4f4e-92ee-bdeac230467d.png" width="598" height="296">

---

## Stacks
<img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=C&logoColor=white"> <img src="https://img.shields.io/badge/Raspbian-A22846?style=for-the-badge&logo=Raspberry Pi&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
