# slack-night-mode-css
Slack Night Mode CSS
Installing
Find your Slack’s application directory.

Windows: %homepath%\AppData\Local\slack\
Mac: /Applications/Slack.app/Contents/
Linux: /usr/lib/slack/ (Debian-based)
Open up the most recent version then  append the following to resources/app.asar.unpacked/src/static/ssb-interop.js:

document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/laCour/slack-night-mode/master/css/raw/black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
