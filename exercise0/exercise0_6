```mermaid

sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Send status code 201 Created
    deactivate server
    
    Note right of browser:: Updates the temporary memory of the browsers notes list
    
    Note right of browser: The browser starts executing the JavaScript code that makes it able to update the temporary notes list 
    
    Note right of browser: At page refresh, the browser would get the data from updated server side. Temporary browser memory would be wiped.

```
