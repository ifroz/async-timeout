# async-timeout

    var timeout = require('async-timeout');
    async.parallel([
      timeout(function noop(){
        // never call back
      }, 1000, 'FALLBACK RESP IN CASE OF TIMEOUT')
    ], function(err, res) {
      console.log(res[0]);
    });