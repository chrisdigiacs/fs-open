sequenceDiagram

    participant browser
    participant server

    Note right of browser: Event handler catches form submission event and handles rendering new note to the page using redraw function

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    Note right of browser: This request contains the new note encoded in a JSON object

    server-->>browser: 201 Created... no redirect, stay on same page
    deactivate server
