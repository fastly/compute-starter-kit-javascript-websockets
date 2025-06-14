# Fastly Compute WebSockets starter kit for JavaScript

[![Deploy to Fastly](https://deploy.edgecompute.app/button)](https://deploy.edgecompute.app/deploy)

Learn about Fastly Compute with WebSockets using a basic starter that sends connections to a backend.

Note: The WebSockets feature handles passthrough connections only. If you want to handle WebSocket connections from clients without having to run a WebSocket backend, see the [Fanout Starter Kit](https://github.com/fastly/compute-starter-kit-javascript-fanout).

**For more details about this and other starter kits for Compute, see the [Fastly Documentation Hub](https://www.fastly.com/documentation/solutions/starters/)**.

## Setup

The app expects a configured backend named `backend` that points to a WebSocket server. For example, if the WebSocket server is available at domain `websockets.example.com`, then you'll need to create a backend on your Compute service named `backend` with the destination host set to `websockets.example.com` and port 443. Also set 'Override Host' to the same host value.

After deploying the app and setting up the backend configuration, all connections received by the service will be passed to the backend.

## Note

This app is not currently supported in Fastly's [local development server](https://www.fastly.com/documentation/guides/compute/testing/#running-a-local-testing-server), as the development server does not support WebSockets features. To experiment with WebSockets, you will need to publish this project to your Fastly Compute service, using the `fastly compute publish` command.

## Security issues

Please see [SECURITY.md](SECURITY.md) for guidance on reporting security-related issues.
