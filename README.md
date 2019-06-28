# redux-voting-app

A React app that allows users to vote for things and uses Redux.

Based on the tutorial found at
http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html.

## How to use

```
npm install
npm test
npm run dev
```

This will start a server at http://localhost:8080/.

To view the results of a vote, visit http://localhost:8080/#/results.

## How it works

The app is implemented using React components with state being managed by a
Redux store. Action creators are used to connect each component to the store
and reducers are used to transform the state when the user interacts with the
app and when the server emits updated data.

A custom piece of middleware called `RemoteActionMiddleware` emits actions to
the server when necessary.

The client and server talk to each other using web sockets implemented by
Socket.io.

The server is implemented using Socket.io so multiple clients can easily
participate in each vote. The server emits a `state` event whenever data changes
and listens to `action` events to store votes from the clients.

## License

MIT
