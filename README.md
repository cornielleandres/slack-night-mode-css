# Slack Night Mode CSS

## Installing

1. Find your Slack’s application directory:

    > **Windows:** %homepath%\AppData\Local\slack\
    > **Mac:** /Applications/Slack.app/Contents/\
    > **Linux:** /usr/lib/slack/ (Debian-based)

2. Open up the most recent version then  append the following to `resources/app.asar.unpacked/src/static/ssb-interop.js`:

    > document.addEventListener('DOMContentLoaded', function() { \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $.ajax({ \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; url: 'https://raw.githubusercontent.com/cornielleandres/slack-night-mode-css/master/slack-night-mode.css', \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; success: function(css) { \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $("<style></style>").appendTo('head').html(css); \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } \
    > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }); \
    > });

3. Save, then re-open Slack.