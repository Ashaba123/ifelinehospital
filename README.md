# ifelinehospital
Cordial Care is an application to have patients consult with doctors remotely.

- [Cordial Care App](#cordial-care-app)
    - [Server](#server)
    - [Mobile App](#mobile-app)
    - [Admin App](#admin-app)
    - [WebRTC server](#webrtc-server)
  - [Installation](#installation)
  - [Running](#running)
    - [Starting](#starting)
    - [Stopping](#stopping)
  
# Cordial Care App

Cordial Care is an application to have patients consult with doctors remotely.

### Server

The server backend is implemented in PHP (Symfony):

**Folder:** `lifeline_backend`

[Backend Server information](lifeline_backend/README.md)

### Mobile App

The Android and iOS frontend is implemented in Dart (Flutter):

**Folder:** `lifeline_mobile`

[Mobile App information](lifeline_mobile/README.md)

### Admin App

The adminitrator frontend is implemented in Javascript (ReactJS):

**Folder:** `lifeline_admin`

[Admin App information](lifeline_admin/README.md)

### WebRTC server

The WebRTC server is an implementation of [flutter-webrtc-server](https://github.com/flutter-webrtc/flutter-webrtc-server)):

**Folder:** `lifeline_webrtc`

[WebRTC server information](lifeline_webrtc/README.md)


## Installation

To get both the server and mobile code run:

```
git clone git@bitbucket.org:victorium/lifeline-telemedicine.git
```

## Running

To simplify running everything correctly you can use `docker-compose`.

### Starting

As long as you have installed Docker desktop or docker run:

```
cd ./docker
docker-compose up --build
```

This will run:

1. The REST API Server (Symfony PHP / Apache application)
2. The Chat Server (ReactPHP server application)
3. The WebRTC TURN server (Go lang application)
4. The Admin Server (ReactJS application)

### Stopping

In another terminal you can run:

```
cd ./docker
docker-compose down
```
