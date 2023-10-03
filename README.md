# Baatein
---------------------------------------------------------

This is a cross platform real time chat application built with HTML, CSS, JavaScript, NodeJS and socket.io
The frontend of this is hosted on vercel and the backend i.e. the server is hosted on Render. 
The server is containing all the necessary initialisations and 'require' statements etc. The server's repository is built separately; you can access here - https://github.com/AtharvA20003/Baatein-backend
---------------------------------------------------------
For running it on localhost, just take the 'index.js' from 'Baatein-backend' and paste it in your new js file(say server). Now run:
1. `npm init -y`
2. `npm i socket.io socket.io-client`

After that take the index.html, style.css and client.js from here. and paste into same directory (you may need to change the path to files according to your directory structure)
1 `major` change which you should do in `server.js`:
```
const PORT = 8000;
const io = require('socket.io')(8000, {
  cors:{
    origin:'*',
  }
})
//rest code similarly
```

In `client.js`:
```const socket = io('http://localhost:8000');```

In `index.html`:
Before `<script src = "client.js"></script>`, you should add:
`<script src = "http://localhost:8000/socket.io/socket.io.js"></script>`

And then in the terminal run: `node server.js`
And then you can open the live server for index.html

---------------------------------------------------------
If you are interacting with the hosted page (baatein-theta.vercel.app) then you can open the hosted link in two of your devices/two of the browser windows and then just wait for the prompt for name to appear. It takes like nearly a minute initially because the server starts on the other site. Then you can enter your name in both(or more) devices/windows/tabs etc. You will get a notification informing who joined and who left(if someone). You can also send a message and it will appear to all of your devices with a pleasant 'Ting'



# Thank you for giving time to my project.
