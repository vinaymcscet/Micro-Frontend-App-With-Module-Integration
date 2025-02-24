# Micro-Frontend-App-With-Module-Integration

This project demonstrates a micro-frontend architecture using module federation. It consists of two main parts: a host application and a remote application.

## Host Application

The host application is a React application that consumes a remote component from the remote application.

### Key files

-   [host/webpack.config.js](host/webpack.config.js): Configures webpack to use module federation, defining the remote application.
-   [host/src/App.js](host/src/App.js): Uses React.lazy and Suspense to dynamically load the remote component.

### Running the Host Application

1.  Navigate to the `host` directory: `cd host`
2.  Install dependencies: `npm install`
3.  Start the development server: `npm start`
4.  Open [http://localhost:3000](http://localhost:3000) in your browser.

## Remote Application

The remote application is a React application that exposes a component to be consumed by the host application.

### Key files

-   [remote/webpack.config.js](remote/webpack.config.js): Configures webpack to expose the `RemoteComponent` using module federation.
-   [remote/src/RemoteComponent.js](remote/src/RemoteComponent.js): The React component exposed to the host application.

### Running the Remote Application

1.  Navigate to the `remote` directory: `cd remote`
2.  Install dependencies: `npm install`
3.  Start the development server: `npm start`
4.  Open [http://localhost:3001](http://localhost:3001) in your browser.

## Module Federation

This project uses Webpack's Module Federation plugin to share code between the host and remote applications. The host application dynamically loads the `RemoteComponent` from the remote application at runtime.