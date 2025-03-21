<!DOCTYPE html>
<html>
  <head>
    <title>Smart Business Card</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/AR-js-org/AR.js/aframe/build/aframe-ar.js"></script>
  </head>
  <body style="margin: 0; overflow: hidden;">
    <!-- AR.js + A-Frame 환경 설정 -->
    <a-scene embedded arjs>
      <!-- 3D 공간 안에 영상 띄우기 -->
      <a-assets>
        <video id="company-video" autoplay loop="true" src="assets/mainvideo.mp4" preload="auto"></video>
      </a-assets>
      
      <!-- AR 마커 설정 (명함을 인식하는 마커) -->
      <a-marker preset="hiro">
        <a-video src="#company-video" width="3" height="2" position="0 0 0"></a-video>
      </a-marker>
      
      <!-- 카메라 설정 -->
      <a-entity camera></a-entity>
    </a-scene>
  </body>
</html>
