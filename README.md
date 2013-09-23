# A simple WebRTC Hack

Check out the demo: https://talky.io


### 1. Create our WebRTC object

```js
var webrtc = new SimpleWebRTC({
    // the id/element dom element that will hold "our" video
    localVideoEl: 'localVideo',
    // the id/element dom element that will hold remote videos
    remoteVideosEl: 'remoteVideos',
    // immediately ask for camera access
    autoRequestMedia: true
});
```

### 2. Tell it to join a room when ready

```js
// we have to wait until it's ready
webrtc.on('readyToCall', function () {
    // you can name it anything
    webrtc.joinRoom('your awesome room name');
});
```


