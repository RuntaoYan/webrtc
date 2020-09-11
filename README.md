# webrtc
webrtc playground

https://github.com/cjb/serverless-webrtc

This is a tech demo of using WebRTC without a signaling server -- the WebRTC offer/answer exchange is performed manually by the users, for example via IM. This means that the app can run out of file:/// directly, without involving a web server. You can send text messages and files between peers.

- This example uses stun server, it is not pure serverless example, it is an example without a signalling server.  
>var cfg = {'iceServers': [{'url': 'stun:23.21.150.121'}]},

- The code is not working, some changes are needed. 

- Better use updated adapter.js, jquery and bootstrap. 
><script src="https://webrtc.github.io/adapter/adapter-latest.js"></script>
- code needed to be changed: 
>// video.src = window.URL.createObjectURL(stream)
>>   video.srcObject=stream
>// attachMediaStream(el, e.stream)
>>   el.srcObject = e.stream
      
- <b>TODO: upload working code. </b>

- Another similiar example (in working conditioin as of 2020 september):
https://www.mobilefish.com/download/webrtc/webrtc_noserver.html
  

- This project us webtorrent tracker server for signalling.
https://github.com/chr15m/bugout


See also: 
- rtcpeerconnection.createoffer

https://webrtc.github.io/samples/src/content/peerconnection/create-offer/
https://github.com/webrtc/samples/tree/gh-pages/src/content/peerconnection/create-offer
