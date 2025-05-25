<html lang="ar"><head>
  <meta charset="UTF-8">
  <title>البث المباشر</title>
  <script src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
</head>
<body style="margin:0; background:black; display:flex; justify-content:center; align-items:center; height:100vh">
  <video id="video" controls="" autoplay="" style="width:90%; max-width:800px; border:4px solid #00f; border-radius:20px;" src="blob:null/3fa3ba01-2e70-4035-a77a-e3588660dd94"></video>

  <script>
    const video = document.getElementById('video');
    const streamUrl = 'https://j5pzts4vewch7un8x93byg.cdnshave.net:8443/hls/6snkc.m3u8'; // <-- بدله هنا

    if (Hls.isSupported()) {
      const hls = new Hls();
      hls.loadSource(streamUrl);
      hls.attachMedia(video);
    } else if (video.canPlayType('application/vnd.apple.mpegurl')) {
      video.src = streamUrl;
    }
  </script>

</body></html>
