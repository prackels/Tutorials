# What's mean ASGI and WSGI?!
## WSGI (Web Server Gateway Interface)
- Synchronous API, meaning it handles requests one at a time.
- Primarily used with traditional web applications that don't require real-time connections.
- Supported by numerous popular Python frameworks like Django and Flask.

## ASGI (Asynchronous Server Gateway Interface)
- Asynchronous API, meaning it can process multiple requests concurrently.
- Primarily used with modern web applications that require real-time connections.
- Supported by several modern Python frameworks like Starlette and Channels.