Exercise 0.5 Single page application diagram

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

    browser->>server: GET /exampleapp/data.json
    activate server
    server-->>browser: JSON file
    deactivate server
    
    Note over browser: renders data into list
```