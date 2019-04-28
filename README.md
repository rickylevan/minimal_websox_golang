# Minimal Working Example of WebSockets with Go Server

This is basically the code from this awesome video https://www.youtube.com/watch?v=dniVs0xKYKk&t=317s from TutorialEdge. This is how I finally got a WebSockets Hello World working on my local machine, after several google-searched blog posts failed to deliver. (No pointing fingers...)

This code works, and deployment is easy. But I won't assume it's obvious. Instead, I'll be explicit. 🤓😄 Here goes:

Clone this repository and then navigate to it with two seperate terminals. (Yes, I know you can run a process in the background, *hush*.) You need to have Golang installed already, and also do a `go get github.com/gorilla/websocket` if you haven't yet. You need Python installed to serve the index.html. Yes, you could do this in other ways, but why not give Python some action.

In Terminal A, run `go run main.go`. In Terminal B, run `python -m SimpleHTTPServer 9876`. Then go to your browser and navigate to `localhost:9876` (which is of course usesa number I just happened to choose). Nothing's on the main screen in the browser (cuz this is a minimal example), but open up the console to see "Hello World from the client!" echoed back from the server. In Terminal A, you can also see this in the logs.

# Conclusion

WebSockets are totally the right solution for modern apps that want a bidirectional event stream between client and server. And of course, the first step to getting a technology integrated in your app is successfully compiling and running a minimal working example of that technology.
