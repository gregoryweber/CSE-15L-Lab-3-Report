# Lab Report 2 - Servers and Bugs

## Part 1 - String Server

In this part, I created a server in which we can add messages to using the `/add-message` path, along with the `s=[insert message here]` query. <br/>
<img src="server-code.png" width="600" alt="stringServer code"/>

Here are two screenshots of messages being added. <br/>
![adding hello to message board](message-1.png)

- When first starting up the server, the `main` method is called. It then starts the server with the inputed port number. When the user visits the website (in my example, http://localhost:4000) The `handleRequest` method is then called in order to handle the request from the user.
- The `url` is the most relevant argument for the handle request method. It contains the path and query parameters that are needed for the program to work. The `messages` variable that belongs to the class is also essential to having this program work. It is a single string with all of the messages separated by a line break.
- the `url` is different for this request, as the `s` query parameter has changed to `"hello world"`. Furthermore, the path here is `/add-message`, which allows the program to understand that a message is to be added. <br/>

![adding world to message board](message-2.png)

- Similar to the last request, `handleRequest` is again called. The main method has already been called once to start the program, so only `handleRequest` has been called.
- Again, the relevant argument here is `url`. `messages` as well is very relevant, as explained above.
- Here, `url` is different, as the query parameter `s` is different than the one shown above. Also, `messages` has been updated to include `hello` from the previous request, which persists to this current request.

## Part 2 - Bug Testing
