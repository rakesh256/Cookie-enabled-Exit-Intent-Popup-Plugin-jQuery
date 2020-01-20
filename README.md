# Cookie-enabled-Exit-Intent-Popup-Plugin-jQuery
Cookie enabled Exit Intent Popup Plugin jQuery

Just another 'Exit Popup' plugin built with jQuery that displays a configurable, cookie-enabled popup window when the user is about to leave the current page. The plugin detects the mouse position (when it is moving up to the address bar) and then fires an event to trigger a modal popup.


1. Include the stylesheet stick-to-me.css to style the exit popup.

1
<link rel="stylesheet" href="stick-to-me.css">
2. Add your own content to the exit popup.

<div id="stickLayer" style="display:none;" class="stick_popup">

  <div class="stick_close" onclick="$.stick_close()">X</div>

  <div class="stick_content">

    <h1>Goodbye!</h1>

  </div>

</div>


3. Include jQuery library and the JavaScript file stick-to-me.js at the bottom of the webpage.

<script src="//code.jquery.com/jquery.min.js"></script>
<script src="stick-to-me.js"></script>

4. Initialize the plugin to create a default exit popup when the cursor moves out of view.
$.stickToMe({

  layer:'#stickLayer'     

});

5. You are able to config the exit popup with the following options.
$.stickToMe({
  fadespeed: 400,
  trigger: ['top'],
  maxtime : 0,
  mintime : 0,
  delay: 0,
  interval: 0,
  maxamount : 0,
  cookie :false,
  bgclickclose :true,
  escclose :true,
  onleave :function (e) {},
  disableleftscroll :true  // chrome disable  
});


