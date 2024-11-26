```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
     Note left of server: The server accesses the data in the body of the POST request <br/>and adds the note to the notes array
    server-->>browser: 302 Found (Location: /exampleapp/notes)
    deactivate server
````
