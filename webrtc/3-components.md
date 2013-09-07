!SLIDE small-image

![WebRTC Bestandteile](webrtc-components.png)

!SLIDE

# getUserMedia
## JavaScript Zugriff auf die Webcam!

!SLIDE example1-slide small

# getUserMedia Demo

<video id="ex" autoplay="autoplay">

<script>
  $(".example1-slide").bind("showoff:show", function() {
    navigator.webkitGetUserMedia(
      {video: true, audio: false},
      function(stream) {
        document.getElementById('ex').src =
            webkitURL.createObjectURL(stream);
      }
    );
  });
</script>


!SLIDE small

# getUserMedia Demo

       @@@ javascript
       <video id="ex" autoplay="autoplay">

       <script>
         navigator.webkitGetUserMedia(
           {video: true, audio: false},
           function(stream) {
             document.getElementById('ex').src =
                 webkitURL.createObjectURL(stream);
           }
         );
       </script>



!SLIDE

# PeerConnection
## Verbindung zwischen beiden Teilnehmern

Benötigt einen externen "Signaling-Kanal"

Nutzbar für Audio/Video und Daten ("Data Channels")
