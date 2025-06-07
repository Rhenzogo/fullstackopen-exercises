sequenceDiagram
```mermaid
    participant user   
    participant browser
    participant server

    user->> browser: Add a new note click Save
        

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: HTML document
    deactivate server
     
   
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: {"content":"wo wowo","date":"2025-05-26T19:15:39.348Z"}
    deactivate server

    