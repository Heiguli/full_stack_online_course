```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST  input from user https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: 302, server asks browser to perform a new HTTP get request at the location /exampleapp/notes
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/exampleapp/notes
    activate server
    server-->>browser: the html file 
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the css file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1", "updated user input"}, ... ]
    deactivate server

    Note right of browser: The browser executes the callback function that renders the updated notes
    ```
