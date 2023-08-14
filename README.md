## Demo

https://aeykeyzs.github.io/speech-to-text/

## Follow
for more tips and tricks

Subscribe to my YouTube Channel: https://www.youtube.com/@snippetzz

And follow me on instagram: https://www.instagram.com/snippet.zz/

# Speech To Text JS



The is a simple real time speech to text interface. It has only HTML and a JS file.

Just import the JavaScript file in your HTML, handle the click events, and you are good to go.

Works with almost every framework. Tested with:

✅ vanillaJS
✅ Vue.js
✅ Angular
✅ ReactJS.

Only these 2 lines of HTML are required to display the recognized intermediate and final text.

``` html
<span id="finalVoiceText"></span>&nbsp;
<span id="interVoiceText"></span>
```

The above 2 html element's IDs are getting used in the 'testSpeech.js' JavaScript file. You can refactor them on your choice.

To create support for frameworks, the methods are exported like below. You can add/ edit the methods as per your requirements:

``` javascript
var tspSocket = (function () {
    return {
        // to start the speech recognition
        grantPermission: function (lang) {
            grantPermissionF(lang);
        },
        // to pause
        stopRecording: function () {
            stopRecordingF();
        },
        // to send text over API/ Backend
        sendText: function () {
            sendRecording();
        }
    }
})(tspSocket || {})
```

In your HTML, or main JavaScript file, you need to import the 'testSpeech.js' JavaScript file and bind the click events to the above methods. Basic example is:

``` html
<script type="text/javascript">
    function clickListenStart() {
        tspSocket.grantPermission('en-US');
    }

    function clickListenPause() {
        tspSocket.stopRecording();
    }
</script>
```

For more documentation over JavaScript functionality, refer to the 'testSpeech.js' JavaScript file.