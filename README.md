wordfeud-api.js
===============

A package for communicating with the Wordfeud-servers

## Usage

```
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

api.acceptInvite
api.chat
api.defaultOptions
api.getBoard
api.getChat
api.getGame
api.getGames
api.getNotifications
api.getRelationships
api.getRuleset
api.getStatus
api.init
api.inviteRandom
api.inviteUser
api.isEmail
api.login
api.loginWithId
api.move
api.pass
api.rejectInvite
api.resign
api.swap

