wordfeud-api.js
===============

A package for communicating with the Wordfeud-servers

## Usage

```javascript
var Api = require('wordfeud-api');
var api = new Api();
api.login('USERNAME/EMAIL', 'PASSWORD', function(err, result) {
    if (err) return console.log(err);
    api.getGames(result.sessionId, function(err, games) {
        if (err) return console.log(err);
        console.log(games);
    });
});
```

## API methods

### Logging in

#### api.defaultOptions(path, contentLength, sessionid)

Default options for the HTTP requests against the WordFeud server.

#### api.init(boards, rulesets)

#### api.login(user, password, onComplete)

#### api.loginWithId(id, password, sessionId, onComplete)


### Games

#### api.getBoard(boardId, sessionId, onComplete)

#### api.getGame(gameId, sessionId, onComplete)

#### api.getGames(sessionId, onComplete)



### Game invites

#### api.acceptInvite(inviteId, sessionId, onComplete)

#### api.getRelationships(sessionId, onComplete)

#### api.inviteRandom(rulesetId, boardType, sessionId, onComplete)

#### api.inviteUser(user, rulesetId, boardType, sessionId, onComplete)

#### api.rejectInvite(inviteId, sessionId, onComplete)



### Chat

#### api.chat(gameId, message, sessionId, onComplete)

#### api.getChat(gameId, sessionId, onComplete)



### Moves

#### api.move(gameId, rulesetId, move, words, sessionId, onComplete)

#### api.pass(gameId, sessionId, onComplete)

#### api.resign(gameId, sessionId, onComplete)

#### api.swap(gameId, tiles, sessionId, onComplete)



### Others


#### api.getNotifications(sessionId, onComplete)

#### api.getRuleset(rulesetId, sessionId, onComplete)

#### api.getStatus(sessionId, onComplete)

