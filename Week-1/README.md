# How browers work?

When a user enters an URL in the browser, how does the browser fetch the desired result?

You type a URL in your browser and press Enter.  
Browser looks up IP address for the domain.  
Browser initiates TCP connection with the server.  
Browser sends the HTTP request to the server.  
Server processes request and sends back a response.  
Browser renders the content.  
### What is the main functionality of the browser?  
The main functionality of browsers is to retrieve information from the World Wide Web and making it available for users.

### High Level Components of a browser.  
The browser's main components are:  
#### The user interface:
this includes the address bar, back/forward button, bookmarking menu, etc. Every part of the browser display except the window where you see the requested page.  
#### The browser engine:  
actions between the UI and the rendering engine.
#### The rendering engine:  
responsible for displaying requested content. For example if the requested content is HTML, the rendering engine parses HTML and CSS, 
and displays the parsed content on the screen.
#### Networking:  
for network calls such as HTTP requests, using different implementations for different platform behind a platform-independent interface.
#### UI backend:  
used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. 
Underneath it uses operating system user interface methods.
#### JavaScript interpreter:  
Used to parse and execute JavaScript code.  
#### Data storage:  
This is a persistence layer. The browser may need to save all sorts of data locally, such as cookies. Browsers also support storage mechanisms such as
localStorage, IndexedDB, WebSQL and FileSystem.


