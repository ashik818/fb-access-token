# fb-access-token
Retrieve facebook access token by Graph API Explorer API.


## Install:
```
npm install fb-access-token
```

## Usage:

### Command line:

```
fbtoken <USERNAME> <PASSWORD> [APP_ID]
```

### Require It:

```javascript
var FbToken = require('fb-access-token')

// login and get access token
// get token for general use by filling 145634995501895 for APP_ID
var fbToken = new FbToken('USERNAME', 'PASSWORD', 'APP_ID')
fbToken.loginGetToken(function (err, token) {
  if (err) throw err

  console.log('Access token:', token)
})

// get token every second without login again
setInterval(function () {
  fbToken.getToken(function (err, token) {
    if (err) throw err

    console.log('Access token in every second:', token);
  })
}, 1000)

```

### Feel free to open issues and PRs
