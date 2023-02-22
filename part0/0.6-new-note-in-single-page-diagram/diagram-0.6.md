Exercise 0.6 New note in single page application diagram

```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: HTTPS GET /exampleapp/spa
    activate server
    server-->>browser: HTML document
    deactivate server
    
    browser->>server: HTTPS GET /exampleapp/main.css
    activate server
    server-->>browser: CSS file
    deactivate server
    
    browser->>server: HTTPS GET /exampleapp/spa.js
    activate server
    server-->>browser: JavaScript file
    deactivate server

    browser->>server: HTTPS GET /exampleapp/data.json
    activate server
    server-->>browser: JSON file
    deactivate server
    
    Note on browser: Renders data into list
    
    browser->>server: POST /exampleapp/new_note_spa
    activate server

    Note on browser: Adds new data to JSON locally and renders data into new list
```