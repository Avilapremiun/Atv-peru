

<html>
  <head>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/clappr@latest/dist/clappr.min.js"></script>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/clappr-google-ima-html5-preroll-plugin@latest/dist/clappr-google-ima-html5-preroll-plugin.min.js"></script>
    <style>
      .player {
        width: 1000px;
        height: 900px;
        overflow: hidden;
      }
    </style>
  </head>
  <body>
    <div class="player"></div>
    <script>
       (function () {
         var playerElement = document.querySelector('.player');

         var apOpts = {
           timeout: 500,
           inline: false,
           muted: false,
         }

         // Single Inline Linear. See https://developers.google.com/interactive-media-ads/docs/sdks/html5/tags
         var vastTag = '';

         Clappr.Utils.canAutoPlayMedia(function(ap, err){
           var player = new Clappr.Player({
             source: 'https://dysmuyxh5vstv.cloudfront.net/hls/live.m3u8',
             parent: playerElement,
             height: 700,
             width: 1000,
             // Set to false and use plugin autostart option (or set to true if tag is false)
             autoPlay: false,
             plugins: {
               core: [ClapprGoogleImaHtml5PrerollPlugin],
             },
             googleImaHtml5PrerollPlugin: {
               tag: vastTag, // VAST tag URL (or false to disable plugin)
               vpaid: 2, // Default is 0 (0 is DISABLED, 1 is ENABLED and 2 is INSECURE)
               autostart: ap,
             }
           });
         }, apOpts);

       })();
    </script>
<html>

	</body>
	</html>


	</body>
	</html>
