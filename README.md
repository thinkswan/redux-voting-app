# redux-voting-server

A Redux server that allows users to vote for things.

Based on the tutorial found at
http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html.

## How to use

```
git clone git@github.com:thinkswan/redux-voting-server.git
npm install
npm test
npm start
```

This will start a Socket.io server on port 8090.

You must also run the
[redux-voting-client](https://github.com/thinkswan/redux-voting-client) project
alongside this server.

## How it works

The server is implemented using Socket.io so multiple clients can easily
participate in each vote. The server emits a `state` event whenever data changes
and listens to `action` events to store votes from the clients.

State is managed with a Redux store.

## License

MIT
