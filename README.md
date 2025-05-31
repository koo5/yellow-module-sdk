# yellow-module-sdk
## Introduction
The Yellow Module SDK is a JavaScript library designed to facilitate the integration of the Yellow Module into yellow-client.

## Module Structure
A module is defined by an URL. In web client, the module is loaded from the URL in a sandboxed iframe. In native client, yellow provides users a method to load the module from an archive at <plugin URL>/archive.zip, and loads index.html into an iframe. In mobile clients, service.js is loaded into a background service on yellow-client startup.

## Module registration
Once the module is loaded, it can register itself with yellow-client by calling `core.registerModule(moduleDefinition)`. The module definition is an object that contains the following properties:
- `identifier`: A unique identifier for the module.
- `callbacks`: An object containing callback functions that yellow-client can call to interact with the module.
- 