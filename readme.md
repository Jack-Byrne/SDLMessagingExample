## SDL WebEngine App Startup Instructions
1) Place the vanilla JS SDL.min.js file into this directory
1) Request a [Manticore instance](https://smartdevicelink.com/resources/manticore/)
1) From terminal with focus in the example app directory, run `npm install` then `npm start`.
1) Your browser will open the app's index.html file with an example querystring attached to the URL. Replace the querystring values with the appropriate information from Manticore/Core.
1) Click on the app in Manticore and observe the series of `Show` RPCs performed.

Note that in the case where sdl_core doesn't support having a websocket server yet, you would need to perform extra steps. You would need to use a proxy which converts your app's websocket connection to a TCP one, which then connects to core over TCP. There is a proxy.jar file with usage instructions in the example vanilla JS hello-sdl application in this project.
# SDLMessagingExample

## Configure Messaging Server

Clone and follow instructions for starting server here -[Messaging Server Repo](https://github.com/ShobhitAd/messaging_app_server)

## Configure IP Address of messaging server

In index.html change"
```
this._serverIP = "192.168.1.242";
```

Or after connected to SDL Core, there is an option to set the IP address from a menu command using the perform interaction keyboard

## First time starting the app

After launching the app for the first time, a keyboard will be presented asking for the users initials. This will be saved in the localStorage and the user wont be prompted for their initials again. To change the initials of the app user, go to menu > Change Identity