# Official NodeJS Wrapper for MSG91 API 


## Documentation


The documentation for the MSG91 API can be found [here](http://docs.msg91.com/ "MSG91 Docs Homepage")

The Node library v1.0 documentation can be found [here](https://github.com/MSG91/MSG91-node/blob/master/README.md).

## DLT Scrubbing
You can get your content template approved by desginated TRAI authorities. We have made a comprehensive document [here](https://help.msg91.com/article/348-dlt-registration "MSG91 DLT") 

## Documentation


The documentation for the MSG91 API can be found [here](http://docs.msg91.com/ "MSG91 Docs Homepage")

The Node library v1.0 documentation can be found [here](https://github.com/MSG91/MSG91-node/blob/master/README.md).

## Sample Usage

```javascript

var msg91 = require("@walkover/msg91")("API_KEY", "SENDER_ID", "ROUTE_NO" );


/**
 * Mobile number should be with International dialling code. Ex - 91 for India, 44 for UK. 
 *
 * @param {mobileNo} Accepts single number
 * @param {mobileNo} Accepts array of the phone number.
 * @param {mobileNo} Accepts CSV string.
 */

var mobileNo = "XXXXXXXXXX";

var mobileNo = [ "XXXXXXXXXX", "XXXXXXXXXX", "XXXXXXXXXX" ];

var mobileNo =  "XXXXXXXXXX,XXXXXXXXXX,XXXXXXXXXX";

msg91.send(mobileNo, "MESSAGE", "DLT_TE_ID", function(err, response){
    console.log(err);
    console.log(response);
});
```




### Get Balance for a route

```javascript
// Default 
msg91.getBalance(function(err, msgCount){
    console.log(err);
    console.log(msgCount);
});

// Get Balance for given Route.
msg91.getBalance("ROUTE_NO", function(err, msgCount){
    console.log(err);
    console.log(msgCount);
});
```

## Getting help

Please reach out to us on support@msg91.com


# MSG91 Variables


### ROUTE_NO
```javascript
1 - Promotional Route
4 - Transactional Route
106 - SendOTP Route
```
