# Racks.js
### a javascript SDK for the Rackspace Cloud
by Seandon Mooy and Matt Ellsworth

  This is the offical renaming of "raxjs" - additionally, it is based on the previously titled "v2" branch. This repo is currently under heavy construction in an attempt to get the rewrite up to speed with raxjs v1.

### Usage
    var RacksJS = require('../racks.js');
    new RacksJS({
        username: 'Rackspace Username',
        apiKey: 'Rackspace API KEY'
    }, function (rack) {
        //Authentication error?
        if (rack.error) {
            return false;
        }
        // rack.PRODUCT.all (.where(), .find(), .create())
        rack.cloudServersOpenStack.servers.all(function (servers) {
            console.log(servers);
        });
    });

### Important info
This repo is not an official rackspace SDK and as such don't expect anyone to support it! (outside of this github). Unless you're messing around with experimental code, I highly recommend using nodejitsu's pkgcloud.

Rack.js is by design, not abstracted away from rackspace's cloud API (docs.rackspace.com). It will never work with other prodivers, but rather, acts as a direct one-to-one documentation-to-functionality javascript bridge. Unlike many other cloud SDKs, there is no invented vocabulary - just product names.

Feel free to issue pull requests :) Thanks!

- Seandon Mooy