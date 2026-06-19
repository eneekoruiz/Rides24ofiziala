# Rides24

Java ride-sharing application with Swing UI, web services, and object database persistence.

## What it includes

- driver, passenger, and administrator flows
- ride lifecycle and booking logic
- Swing desktop interface
- SOAP web service exposure in remote mode
- unit and integration tests
- GitHub Actions and SonarCloud

## Architecture

The Swing interface delegates ride operations to a business facade. ObjectDB stores local domain data, while JAX-WS clients isolate calls to external ride services so remote communication does not leak into UI event handlers.

## Links

- DeepWiki: https://deepwiki.com/eneekoruiz/Rides24ofiziala
