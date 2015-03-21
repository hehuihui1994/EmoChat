# Emotion Enhanced Chat

EmoChat is the 1st place winner of a 2-days hackthon named [Brainihack](http://brainihack.org/).
This project is based on [OpenTokRTC](https://github.com/opentok/OpenTokRTC) and enhances with **emotion detection
capabilities** using **NeuroSteer** EEG headset.

The idea is to detect the user emotion using live EEG feed and enable emotion sharing over the chat room by
gestures like emojis next to chat line and color changes according to peer's mode.

## File Overview
* `Procfile` is required to run the nodejs app on Heroku
* `package.json` contains all npm modules to run the app
* `app.js` contains all server side code  
* `config.js` contains configurations: TokBox credentials, p2p mesh support, Redis support, reserved rooms, etc.  
* `lib` folder contains all the code to handle configurations: p2p mesh support, Redis support, reserved rooms, etc.   
* `views` folder contains the html template for the app
* `public/css` folder contains all the css for the app.    
  Look for files with `.scss` extensions. `.css` files are generated from sass.
* `public/js` contains the front end code and interactions with OpenTok SDK.  

## How to run the app:
1. Clone [this repo]( https://github.com/opentok/OpenTokRTC )  
2. Get my API Key and Secret from [TokBox]( http://TokBox.com )  
3. Replace `OTKEY` and `OTSECRET` with your corresponding API Key and Secret in `config.js` or by setting your env variables
4. Run `npm install` to install the necessary packages  
5. Start the server with `node app.js`  

## How to use:

1. In the chat main screen (usaly localhost:9393) enter a room name (anything would do)
2. type in the chat /help to get a list of configurations available
3. To link the NeuroSteer headset with the current chat user type `/user <last 6 digits of the headset serial #>`

## Additional links:

1. https://vimeo.com/122224388 - presentation at Brainihack final demo
2. https://vimeo.com/122826001 - screen capture of a chat we did in Brainhack's final demo
