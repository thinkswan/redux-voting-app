# redux-voting-client

A Redux app that allows users to vote for things.

Based on the tutorial found at
http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html.

## How to use

```
git clone git@github.com:thinkswan/redux-voting-client.git
npm install
npm test
npm start
```

This will start a server at http://localhost:8080/.

To view the results of a vote, visit http://localhost:8080/#/results.

You must also run the
[redux-voting-server](https://github.com/thinkswan/redux-voting-server) project
alongside this client.

## How it works

The app is implemented using React components with state being managed by a
Redux store. Action creators are used to connect each component to the store
and reducers are used to transform the state when the user interacts with the
app and when the server emits updated data.

A custom piece of middleware called `RemoteActionMiddleware` emits actions to
the server when necessary.

The client and server talk to each other using web sockets implemented by
Socket.io.

## License

MIT
