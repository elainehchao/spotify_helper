# Spotify Helper Application

## Installation

### Using your own credentials
You will need to register your app and get your own credentials from the Spotify for Developers Dashboard.

To do so, go to [your Spotify for Developers Dashboard](https://beta.developer.spotify.com/dashboard) and create your application. For the examples, we registered these Redirect URIs:

* http://localhost:8888 (needed for the implicit grant flow)
* http://localhost:8888/callback

Once you have created your app, create a file `credentials.js` in the root directory and add the following contents: 

```
var CLIENT_ID = '<client_id>'; // Your client id
var CLIENT_SECRET = '<client_secret>'; // Your secret
var REDIRECT_URI = '<redirect_uri>'; // Your whitelisted redirect uri

module.exports.CLIENT_ID = CLIENT_ID;
module.exports.CLIENT_SECRET = CLIENT_SECRET;
module.exports.REDIRECT_URI = REDIRECT_URI;
```

replace the `client_id`, `redirect_uri` and `client_secret` in the examples with the ones you get from My Applications.

## Running the examples
In order to run the different examples, open the folder with the name of the flow you want to try out, and run its `app.js` file. For instance, to run the Authorization Code example do:

    $ cd authorization_code
    $ node app.js

Then, open `http://localhost:8888` in a browser.
