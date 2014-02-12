Coindesk Node
=======

Unofficial Node JS client for the CoinDesk API

Installing
----------

```
npm install coindesk-node
```
Example usage
-------------
Quick usage: Get the current prices in USD
```javascript
CoinBase = require("./index.js");
coindesk = new CoinBase();
coindesk.currentPrice(null,function(data){
  console.log(data);
});
```
It is possible to set un another currency
```javascript
CoinBase = require("./index.js");
coindesk = new CoinBase({currency: "EUR"});
```
Retrieve historical data
```javascript
CoinBase = require("./index.js");
coindesk = new CoinBase();
var start_date = new Date();
var end_date = new Date();
end_date.setDate(end_date.getDate() - 60);
coindesk.historical({start_date: new Date(), end_date: end_date }, null, function(data) {
  console.log(data);
});
```