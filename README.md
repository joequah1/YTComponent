# YTComponent

Youtube Component - Build youtube Iframe API and State Change Events in Object Oriented. 
Usage is as easy as init a function. 
The youtube has included necessary tracker in each event state.

## Installation 

A div tag with ID, the ID is required when initalizing the ytComponent 

    <div id="yt_frame"></div>

Import the js file 

    <script src="js/ninjoe.ytComponent.js"></script>

## Usage

### Basic Usage 

Initialize the ytComponent 

    var  app = new ytComponent({
        'container' : 'yt_frame',
        'width' : '640',
        'height' : '390',
        'videoId' : 'M7lc1UVf-VE'
    });
    
Include the onYouTubeIframeAPIReady function after initializing ytComponent

    function onYouTubeIframeAPIReady() {
        app.loadVideo();
    }
        
This function is required for Youtube Iframe API, the API will call to this function when the page has finished download the Javascript for the player API.
Do remember to change the variable named app if necessary. 

### Tracking 

To track for each event state

    var tracker = function (type) {
        // tracker function 
    }
    
    var  app = new ytComponent({
        'container' : 'yt_frame',
        'width' : '640',
        'height' : '390',
        'videoId' : 'M7lc1UVf-VE',
        'tracker' : tracker
    });

### Autoplay 

To autoplay youtube video, autoplay will only works in desktop browser

    var  app = new ytComponent({
        'container' : 'yt_frame',
        'width' : '640',
        'height' : '390',
        'videoId' : 'M7lc1UVf-VE',
        'autoplay' : true
    });

## Thanks 
Currying - http://www.dustindiaz.com/javascript-curry/
