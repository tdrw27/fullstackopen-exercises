# New Note Submission Diagram
```mermaid
sequenceDiagram
Browser->>Server: Form is clicked and browser sends HTTP POST request. Data is submitted.
Note right of Server: Processes the data based on the code living in the server.
Server->>Browser: Server responds status code 302 - URL Redirect. Asks browser to do new HTTP GET request to location in header.
Note left of Browser: Reloads page causing 3 more requests.
Browser->>Server: Request stylesheet, javascript, and json data.
Server->>Browser: Responds to requests.
Note left of Browser: Loads page.
```
