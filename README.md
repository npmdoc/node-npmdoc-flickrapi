# api documentation for  [flickrapi (v0.6.0)](https://github.com/Pomax/node-flickrapi#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-flickrapi.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-flickrapi) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-flickrapi.svg)](https://travis-ci.org/npmdoc/node-npmdoc-flickrapi)
#### A Node.js, and client-side, implementation of the Flickr API (for use with an API key, server-side oauth enabled)

[![NPM](https://nodei.co/npm/flickrapi.png?downloads=true)](https://www.npmjs.com/package/flickrapi)

[![apidoc](https://npmdoc.github.io/node-npmdoc-flickrapi/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-flickrapi_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-flickrapi/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-flickrapi/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-flickrapi/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Pomax",
        "email": "pomax@nihongoresources.com"
    },
    "bugs": {
        "url": "https://github.com/Pomax/node-flickrapi/issues"
    },
    "dependencies": {
        "async": "~0.2.10",
        "glob": "~3.2.6",
        "open": "0.0.x",
        "progress": "1.1.4",
        "prompt": "0.2.x",
        "request": "2.26.x"
    },
    "description": "A Node.js, and client-side, implementation of the Flickr API (for use with an API key, server-side oauth enabled)",
    "devDependencies": {
        "express": "~3.4.7",
        "grunt": "~0.4.1",
        "grunt-contrib-jshint": "~0.6.3",
        "grunt-contrib-nodeunit": "~0.2.0",
        "grunt-contrib-uglify": "~0.2.2",
        "habitat": "~1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "590400e27758828337daf269d93b5ea78816635f",
        "tarball": "https://registry.npmjs.org/flickrapi/-/flickrapi-0.6.0.tgz"
    },
    "engines": {
        "node": ">=0.12"
    },
    "gitHead": "6c3acbb7606e7e97de928feac98758dc5521ec18",
    "homepage": "https://github.com/Pomax/node-flickrapi#readme",
    "keywords": [
        "flickrapi",
        "flickr",
        "api",
        "oauth"
    ],
    "license": "MIT",
    "main": "./src/FlickrAPI",
    "maintainers": [
        {
            "name": "pomax",
            "email": "pomax@nihongoresources.com"
        }
    ],
    "name": "flickrapi",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Pomax/node-flickrapi.git"
    },
    "scripts": {
        "test": "node test"
    },
    "version": "0.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module flickrapi](#apidoc.module.flickrapi)
1.  [function <span class="apidocSignatureSpan">flickrapi.</span>authenticate (options, next)](#apidoc.element.flickrapi.authenticate)
1.  [function <span class="apidocSignatureSpan">flickrapi.</span>downsync (location, removeDeleted)](#apidoc.element.flickrapi.downsync)
1.  [function <span class="apidocSignatureSpan">flickrapi.</span>loadLocally (location, options)](#apidoc.element.flickrapi.loadLocally)
1.  [function <span class="apidocSignatureSpan">flickrapi.</span>tokenOnly (options, next)](#apidoc.element.flickrapi.tokenOnly)
1.  [function <span class="apidocSignatureSpan">flickrapi.</span>upload ()](#apidoc.element.flickrapi.upload)
1.  object <span class="apidocSignatureSpan">flickrapi.</span>Utils

#### [module flickrapi.Utils](#apidoc.module.flickrapi.Utils)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>checkRequirements (method_name, required, callOptions, callback)](#apidoc.element.flickrapi.Utils.checkRequirements)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>encodeRFC5987ValueChars (str)](#apidoc.element.flickrapi.Utils.encodeRFC5987ValueChars)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>formQueryString (queryArguments)](#apidoc.element.flickrapi.Utils.formQueryString)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateAPIDevFunction (method)](#apidoc.element.flickrapi.Utils.generateAPIDevFunction)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateAPIFunction (method)](#apidoc.element.flickrapi.Utils.generateAPIFunction)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateQueryArguments (method_name, flickrOptions, callOptions)](#apidoc.element.flickrapi.Utils.generateQueryArguments)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>handleURLRequest (verb, url, processResult, postdata)](#apidoc.element.flickrapi.Utils.handleURLRequest)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryFlickr (queryArguments, flickrOptions, security, processResult)](#apidoc.element.flickrapi.Utils.queryFlickr)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryFlickrAPI (queryArguments, flickrOptions, security, processResult)](#apidoc.element.flickrapi.Utils.queryFlickrAPI)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryProxyEndpoint (queryArguments, flickrOptions, processResult)](#apidoc.element.flickrapi.Utils.queryProxyEndpoint)
1.  [function <span class="apidocSignatureSpan">flickrapi.Utils.</span>upload (uploadOptions, flickrOptions, processResult)](#apidoc.element.flickrapi.Utils.upload)



# <a name="apidoc.module.flickrapi"></a>[module flickrapi](#apidoc.module.flickrapi)

#### <a name="apidoc.element.flickrapi.authenticate"></a>[function <span class="apidocSignatureSpan">flickrapi.</span>authenticate (options, next)](#apidoc.element.flickrapi.authenticate)
- description and source-code
```javascript
authenticate = function (options, next) {
  if(!options) {
    process.nextTick(function(){
      next(new Error("Please pass an valid Flickr API key and secret to the Flickr module.\n"+
                     "Visit http://www.flickr.com/services/apps/create/apply to get one."));
    });
    return;
  }

  // out-of-browser authentication unless specified otherwise
  if(!options.callback) { options.callback = "oob"; }
  if(!options.requestOptions) options.requestOptions = {};

  // effect authentication
  checkToken(options, function(err, access) {
    var APIBuilder = require("./flickr-api-object");
    if(!access) {
      requestToken(options, function(err, body) {
        if(options.callback !== "oob") {
          options.processCredentials = options.processCredentials || function(data) {
            // default function writes creds to .env
            if(!options.silent) {
              console.log("Credentials object:");
              console.log(JSON.stringify(data,null,2));
            }
            var envContent = fs.readFileSync(".env") + "\n";
            Object.keys(data).forEach(function(key) {
              envContent += "export " + key + "=" + data[key] + "\n";
            });
            fs.writeFileSync(".env", envContent);
          };
          options.processCredentials(body);
        }

        // is this auth only, or also API object creation?
        if(options.noAPI) {
          process.nextTick(function() { next(false); });
        }
        else { new APIBuilder(options, Utils, next); }
      });
    } else { new APIBuilder(options, Utils, next); }
  });
}
```
- example usage
```shell
...
'''
var Flickr = require("flickrapi"),
    flickrOptions = {
      api_key: "API key that you get from Flickr",
      secret: "API key secret that you get from Flickr"
    };

Flickr.authenticate(flickrOptions, function(error, flickr) {
  // we can now use "flickr" as our API object
});
'''

### As flickrapi internally uses the request module, you can also pass default options for request that are accepted by request.
defaults() as documented in the [request module](https://github.com/request/request#requestdefaultsoptions)
...
```

#### <a name="apidoc.element.flickrapi.downsync"></a>[function <span class="apidocSignatureSpan">flickrapi.</span>downsync (location, removeDeleted)](#apidoc.element.flickrapi.downsync)
- description and source-code
```javascript
downsync = function (location, removeDeleted) {
  "use strict";

  location = location || "./data";
  removeDeleted = removeDeleted || false;

  var fs = require("fs"),
      aggregatePhotos = require("./photos");

  // directory structure
  var data = require("../ia")(location);

  // process calls
  var photos = require("./photos");
  var sets = require("./sets");
  var collections = require("./collections");

  // Kick off the down-syncing process
  return function(err, flickr) {
    if(err) { return console.log(err); }

    flickr.options.locals = data;

    var completed = function() {
      console.log("Finished downsyncing.");
      var handler = flickr.options.afterDownsync;
      if (handler) { handler(); }
      else { process.exit(0); }
    };

    console.log();
    collections(flickr, function() {
      sets(flickr, function() {
        photos(flickr, completed);
      });
    });
  };
}
```
- example usage
```shell
...
## Download data from Flickr

You can use this module to very easily download all your Flickr content, using the built in 'downsync' function:

'''
var Flickr = require("flickrapi"),
    flickrOptions = { ... };
Flickr.authenticate(flickrOptions, flickrapi.downsync());
'''

That's all you need to run. The package will generate a data directory with your images in './data/images' (in several sizes), and
 the information architecture (metadata, sets, collections, etc) in './data/ia'.

If you want this in a different directory, you can pass the dir as an argument to the downsync function:

'''
...
```

#### <a name="apidoc.element.flickrapi.loadLocally"></a>[function <span class="apidocSignatureSpan">flickrapi.</span>loadLocally (location, options)](#apidoc.element.flickrapi.loadLocally)
- description and source-code
```javascript
loadLocally = function (location, options) {
  options = options || {};
  var dirstructure = ensureDirectories(location);

  // photos are ranked by publication date
  var photos = readAll(dirstructure.ia.photos.root, "id", function(a,b,items) {
    return items[b].dates.posted - items[a].dates.posted;
  });

  // sets are ranked by creation date
  var photosets = readAll(dirstructure.ia.photosets, "id", function(a,b,items) {
    return items[b].date_create - items[a].date_create;
  });

  // collections are sorted alphabetically
  var collections = readAll(dirstructure.ia.collections, "id", function(a,b,items) {
    a = items[a].title;
    b = items[b].title;
    return a === b ? 0 : b < a ? -1 : -1;
  });

  // filter out the private photos from the key index
  if(!options.loadPrivate) {
    photos.keys = photos.keys.filter(function(key) {
      return photos.data[key].visibility.ispublic === 1;
    });
    photosets.keys = photosets.keys.filter(function(key) {
      return photosets.data[key].visibility_can_see_set === 1;
    });
  }

  // perform cross-referencing
  crossReference(dirstructure, photos, photosets, collections);

  // our final IA object
  return {
    // photos
    photos: photos.data,
    photo_keys: photos.keys,
    // sets
    photosets: photosets.data,
    photoset_keys: photosets.keys,
    // collections
    collections: collections.data,
    collection_keys: collections.keys,
    // dir adminstration
    dirstructure: dirstructure
  };
}
```
- example usage
```shell
...

## Use your Flickr data in another application

If you downloaded all your Flickr data, you can use these in your own node apps by "dry loading" Flickr:

'''
var Flickr = require("flickrapi"),
  flickrData = Flickr.loadLocally();
'''

This will give you an object with the following structure:

'''
{
photos: [photo objects],
...
```

#### <a name="apidoc.element.flickrapi.tokenOnly"></a>[function <span class="apidocSignatureSpan">flickrapi.</span>tokenOnly (options, next)](#apidoc.element.flickrapi.tokenOnly)
- description and source-code
```javascript
tokenOnly = function (options, next) {
  if(!options) {
    return next(new Error("Please pass an valid Flickr API key and secret to the Flickr module.\n"+
                          "Visit http://www.flickr.com/services/apps/create/apply to get one."));
  }

  if(!options.requestOptions) options.requestOptions = {};
  var APIBuilder = require("./flickr-api-object");
  options.tokenonly = true;
  new APIBuilder(options, Utils, next);
}
```
- example usage
```shell
...
'''
var Flickr = require("flickrapi"),
    flickrOptions = {
      api_key: "API key that you get from Flickr",
      secret: "API key secret that you get from Flickr"
    };

Flickr.tokenOnly(flickrOptions, function(error, flickr) {
  // we can now use "flickr" as our API object,
  // but we can only call public methods and access public data
});
'''

### Authenticated, full Flickr API access
...
```

#### <a name="apidoc.element.flickrapi.upload"></a>[function <span class="apidocSignatureSpan">flickrapi.</span>upload ()](#apidoc.element.flickrapi.upload)
- description and source-code
```javascript
upload = function () { [native code] }
```
- example usage
```shell
...
    },{
      title: "test2",
      tags: "happy fox image \"test 2\" separate tags",
      photo: __dirname + "/test.jpg"
    }]
  };

  Flickr.upload(uploadOptions, FlickrOptions, function(err, result) {
    if(err) {
      return console.error(error);
    }
    console.log("photos uploaded", result);
  });
});
'''
...
```



# <a name="apidoc.module.flickrapi.Utils"></a>[module flickrapi.Utils](#apidoc.module.flickrapi.Utils)

#### <a name="apidoc.element.flickrapi.Utils.checkRequirements"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>checkRequirements (method_name, required, callOptions, callback)](#apidoc.element.flickrapi.Utils.checkRequirements)
- description and source-code
```javascript
checkRequirements = function (method_name, required, callOptions, callback) {
  required = required || [];
  for(var r=0, last=required.length, arg; r<last; r++) {
    arg = required[r];
    if(arg.name === "api_key") continue;
    if(!callOptions.hasOwnProperty(arg.name)) {
      return callback(new Error("missing required argument '"+arg.name+"' in call to "+method_name));
    }
  }
}
```
- example usage
```shell
...
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback);
  };
},
generateAPIDevFunction: function(method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    Utils.checkRequirements(method.name, method.required, callOptions, callback);
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback, method.errors);
  };
},
generateQueryArguments: function(method_name, flickrOptions, callOptions) {
  // set up authorized method access
  var queryArguments = {
...
```

#### <a name="apidoc.element.flickrapi.Utils.encodeRFC5987ValueChars"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>encodeRFC5987ValueChars (str)](#apidoc.element.flickrapi.Utils.encodeRFC5987ValueChars)
- description and source-code
```javascript
encodeRFC5987ValueChars = function (str) {
  return encodeURIComponent(str).
  replace(/['()!]/g, escape).
  replace(/\*/g, '%2A').
  replace(/%(?:7C|60|5E)/g, unescape);
}
```
- example usage
```shell
...
    replace(/\*/g, '%2A').
    replace(/%(?:7C|60|5E)/g, unescape);
  },
  formQueryString: function(queryArguments) {
    var Utils = this,
        args = [],
        append = function(key) {
          args.push(key + "=" + Utils.encodeRFC5987ValueChars(queryArguments[key]));
        };
    Object.keys(queryArguments).sort().forEach(append);
    return args.join("&");
  },
checkRequirements: function(method_name, required, callOptions, callback) {
  required = required || [];
  for(var r=0, last=required.length, arg; r<last; r++) {
...
```

#### <a name="apidoc.element.flickrapi.Utils.formQueryString"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>formQueryString (queryArguments)](#apidoc.element.flickrapi.Utils.formQueryString)
- description and source-code
```javascript
formQueryString = function (queryArguments) {
  var Utils = this,
      args = [],
      append = function(key) {
        args.push(key + "=" + Utils.encodeRFC5987ValueChars(queryArguments[key]));
      };
  Object.keys(queryArguments).sort().forEach(append);
  return args.join("&");
}
```
- example usage
```shell
...
/**
 * When contacting Flickr "regularly", permission levels greater than 0 (public access)
 * cannot be securely dealt with. read-only, write, and delete all require oauth
 * authentication keys, and these should never, ever, be stored at the client.
 */
queryFlickrAPI: function(queryArguments, flickrOptions, security, processResult) {
  var url = "https://api.flickr.com/services/rest/",
      queryString = this.formQueryString(queryArguments),
      flickrURL = url + "?" + queryString;
  // Do we need special permissions? (read private, 1, write, 2, or delete, 3)?
  // if so, those are currently not supported. Send an error-notification.
  if(security.requiredperms > 0) {
    return processResult(new Error("signed calls (write/delete) currently not supported"));
  }
  this.handleURLRequest("GET", flickrURL, processResult);
...
```

#### <a name="apidoc.element.flickrapi.Utils.generateAPIDevFunction"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateAPIDevFunction (method)](#apidoc.element.flickrapi.Utils.generateAPIDevFunction)
- description and source-code
```javascript
generateAPIDevFunction = function (method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    Utils.checkRequirements(method.name, method.required, callOptions, callback);
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback, method.errors);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.flickrapi.Utils.generateAPIFunction"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateAPIFunction (method)](#apidoc.element.flickrapi.Utils.generateAPIFunction)
- description and source-code
```javascript
generateAPIFunction = function (method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback);
  };
}
```
- example usage
```shell
...
      return +(err.code) < errCap;
    });

// also append the generic error knowledge
Utils.extendErrors(result.errors.error, errCap);

// build the API function
var flickrAPIFunction = Utils.generateAPIFunction(method_name, flickrOptions, security, required, optional, errors);
flickrAPIFunction.security = security;

// bind hierarchically
var curr = API,
    level;
while(hierarchy.length > 0) {
  level = hierarchy.splice(0,1)[0];
...
```

#### <a name="apidoc.element.flickrapi.Utils.generateQueryArguments"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>generateQueryArguments (method_name, flickrOptions, callOptions)](#apidoc.element.flickrapi.Utils.generateQueryArguments)
- description and source-code
```javascript
generateQueryArguments = function (method_name, flickrOptions, callOptions) {
  // set up authorized method access
  var queryArguments = {
    method: method_name,
    format: "json",
  };
  if(flickrOptions.api_key) {
    queryArguments.api_key = flickrOptions.api_key;
  }
  // set up bindings for method-specific args
  Object.keys(callOptions).forEach(function(key) {
    queryArguments[key] = callOptions[key];
  });
  return queryArguments;
}
```
- example usage
```shell
...
      return callback(new Error("missing required argument '"+arg.name+"' in call to "+method_name));
    }
  }
},
generateAPIFunction: function(method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback);
  };
},
generateAPIDevFunction: function(method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    Utils.checkRequirements(method.name, method.required, callOptions, callback);
...
```

#### <a name="apidoc.element.flickrapi.Utils.handleURLRequest"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>handleURLRequest (verb, url, processResult, postdata)](#apidoc.element.flickrapi.Utils.handleURLRequest)
- description and source-code
```javascript
handleURLRequest = function (verb, url, processResult, postdata) {
  var xhr = new XMLHttpRequest();
  xhr.open(verb, url, true);
  if(postdata) {
    xhr.setRequestHeader("Content-Type", "application/json");
  }
  xhr.onreadystatechange = function() {
    if(xhr.readyState === 4) {
      if(xhr.status == 200) {
        var error = false,
            body = xhr.responseText;
        // we get a response, but there's no response body. That's a problem.
        if(!body) {
          error = "HTTP Error " + response.statusCode + " (" + statusCodes[response.statusCode] + ")";
          return processResult(error);
        }
        // we get a response, and there were no errors
        if(!error) {
          try {
            body = body.trim().replace(/^jsonFlickrApi\(/,'').replace(/\}\)$/,'}');
            body = JSON.parse(body);
            if(body.stat !== "ok") {
              // There was a request error, and the JSON .stat property
              // will tell us what that error was.
              return processResult(body.message);
            }
          } catch (e) {
            // general JSON error
            return processResult("could not parse body as JSON");
          }
        }
        // Some kind of other error occurred. Simply call the process
        // handler blindly with both the error and error body.
        processResult(error, body);
      }
      else { processResult("HTTP status not 200 (received "+xhr.status+")"); }
    }
  };
  xhr.send(postdata ? JSON.stringify(postdata) : null);
}
```
- example usage
```shell
...
      queryString = this.formQueryString(queryArguments),
      flickrURL = url + "?" + queryString;
  // Do we need special permissions? (read private, 1, write, 2, or delete, 3)?
  // if so, those are currently not supported. Send an error-notification.
  if(security.requiredperms > 0) {
    return processResult(new Error("signed calls (write/delete) currently not supported"));
  }
  this.handleURLRequest("GET", flickrURL, processResult);
},
/**
 * When we're contacting a Flickr API proxy, we can rely on the fact that it will
 * take care of oauth authentication for us, and so we do not need to do any kind
 * of security permissions check for the requested methods.
 */
queryProxyEndpoint: function(queryArguments, flickrOptions, processResult) {
...
```

#### <a name="apidoc.element.flickrapi.Utils.queryFlickr"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryFlickr (queryArguments, flickrOptions, security, processResult)](#apidoc.element.flickrapi.Utils.queryFlickr)
- description and source-code
```javascript
queryFlickr = function (queryArguments, flickrOptions, security, processResult) {
  if(flickrOptions.endpoint) {
    return this.queryProxyEndpoint(queryArguments, flickrOptions, processResult);
  }
  return this.queryFlickrAPI(queryArguments, flickrOptions, security, processResult);
}
```
- example usage
```shell
...
    }
  }
},
generateAPIFunction: function(method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
    Utils.queryFlickr(queryArguments, this.flickrOptions, method.security, callback);
  };
},
generateAPIDevFunction: function(method) {
  return function(callOptions, callback) {
    if(callOptions && !callback) { callback = callOptions; callOptions = {}; }
    Utils.checkRequirements(method.name, method.required, callOptions, callback);
    var queryArguments = Utils.generateQueryArguments(method.name, this.flickrOptions, callOptions);
...
```

#### <a name="apidoc.element.flickrapi.Utils.queryFlickrAPI"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryFlickrAPI (queryArguments, flickrOptions, security, processResult)](#apidoc.element.flickrapi.Utils.queryFlickrAPI)
- description and source-code
```javascript
queryFlickrAPI = function (queryArguments, flickrOptions, security, processResult) {
  var url = "https://api.flickr.com/services/rest/",
      queryString = this.formQueryString(queryArguments),
      flickrURL = url + "?" + queryString;
  // Do we need special permissions? (read private, 1, write, 2, or delete, 3)?
  // if so, those are currently not supported. Send an error-notification.
  if(security.requiredperms > 0) {
    return processResult(new Error("signed calls (write/delete) currently not supported"));
  }
  this.handleURLRequest("GET", flickrURL, processResult);
}
```
- example usage
```shell
...
  });
  return queryArguments;
},
queryFlickr: function(queryArguments, flickrOptions, security, processResult) {
  if(flickrOptions.endpoint) {
    return this.queryProxyEndpoint(queryArguments, flickrOptions, processResult);
  }
  return this.queryFlickrAPI(queryArguments, flickrOptions, security, processResult);
},
/**
 * If you want to upload, you're going to have to do it server side.
 */
upload: function(uploadOptions, flickrOptions, processResult) {
  return processResult(new Error("Uploading directly from the browser is not supported"));
},
...
```

#### <a name="apidoc.element.flickrapi.Utils.queryProxyEndpoint"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>queryProxyEndpoint (queryArguments, flickrOptions, processResult)](#apidoc.element.flickrapi.Utils.queryProxyEndpoint)
- description and source-code
```javascript
queryProxyEndpoint = function (queryArguments, flickrOptions, processResult) {
  var queryString = this.formQueryString(queryArguments),
      url = flickrOptions.endpoint + "?" + queryString;
  this.handleURLRequest("POST", url, processResult, queryArguments);
}
```
- example usage
```shell
...
  Object.keys(callOptions).forEach(function(key) {
    queryArguments[key] = callOptions[key];
  });
  return queryArguments;
},
queryFlickr: function(queryArguments, flickrOptions, security, processResult) {
  if(flickrOptions.endpoint) {
    return this.queryProxyEndpoint(queryArguments, flickrOptions, processResult);
  }
  return this.queryFlickrAPI(queryArguments, flickrOptions, security, processResult);
},
/**
 * If you want to upload, you're going to have to do it server side.
 */
upload: function(uploadOptions, flickrOptions, processResult) {
...
```

#### <a name="apidoc.element.flickrapi.Utils.upload"></a>[function <span class="apidocSignatureSpan">flickrapi.Utils.</span>upload (uploadOptions, flickrOptions, processResult)](#apidoc.element.flickrapi.Utils.upload)
- description and source-code
```javascript
upload = function (uploadOptions, flickrOptions, processResult) {
  return processResult(new Error("Uploading directly from the browser is not supported"));
}
```
- example usage
```shell
...
    },{
      title: "test2",
      tags: "happy fox image \"test 2\" separate tags",
      photo: __dirname + "/test.jpg"
    }]
  };

  Flickr.upload(uploadOptions, FlickrOptions, function(err, result) {
    if(err) {
      return console.error(error);
    }
    console.log("photos uploaded", result);
  });
});
'''
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
