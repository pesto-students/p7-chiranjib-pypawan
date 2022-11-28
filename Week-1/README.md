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

![high-level-components-of-browsers](https://user-images.githubusercontent.com/64304307/204169685-adc4293e-b55c-479d-b24f-e24693282f45.jpeg)

### Rendering engine and its uses?  
A rendering engine is software that draws text and images on the screen. The engine draws structured text from a HTML document, and formats it properly based on the given style declarations given in CSS. Examples of layout engines: Blink, Gecko, EdgeHTML, WebKit.  

### Parse HTML, CSS and JavaScript.  
Parsing means analyzing and converting a program into an internal format that a runtime environment can actually run, for example the JavaScript engine inside browsers.  
  
The browser parses HTML into a DOM tree. HTML parsing involves tokenization and tree construction. HTML tokens include start and end tags, as well as attribute names and values. If the document is well-formed, parsing it is straightforward and faster. The parser parses tokenized input into the document, building up the document tree.  
  
When the HTML parser finds non-blocking resources, such as an image, the browser will request those Layout computes the exact position and size of each object. resources and continue parsing. Parsing can continue when a CSS file is encountered, but <script> tags—particularly those without an async or defer attribute—blocks rendering, and pauses parsing of HTML.  
    
When the browser encounters CSS styles, it parses the text into the CSS Object Model (or CSSOM), a data structure it then uses for styling layouts and painting. The browser then creates a render tree from both these structures to be able to paint the content to the screen. JavaScript is also downloaded, parsed, and then executed.
  
JavaScript parsing is done during compile time or whenever the parser is invoked, such as during a call to a method.  
    
### Script Processors  
  The script processor executes Javascript code to process an event. The processor uses a pure Go implementation of ECMAScript 5.1 and has no external dependencies. This can be useful in situations where one of the other processors doesn't provide the functionality you need to filter events.  
  
### Render-tree Construction, Layout, and Paint.  
  The DOM and CSSOM trees are combined to form the render tree.  
    
  Render tree contains only the nodes required to render the page.  
    
  Layout computes the exact position and size of each object.  
    
  
  The last step is paint, which takes in the final render tree and renders the pixels to the screen.  
  
   The browser combines the DOM and CSSOM into a "render tree," which captures all the visible DOM content on the page and all the CSSOM style information for each node.
  

