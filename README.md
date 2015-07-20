# anyproxy-wsclient [![spm version](http://spmjs.io/badge/anyproxy-wsclient)](http://spmjs.io/package/anyproxy-wsclient)

---

## About

* this a websocket client for [AnyProxy](https://github.com/alibaba/anyproxy). By using it, you could get noticed on information about the realtime requests going through your proxy server.

* Be sure to launch AnyProxy before using this client.


## Install

```
$ spm install anyproxy-wsclient --save
```

## usage

````javascript
var anyproxyWsclient = require('anyproxy-wsclient');

new anyproxyWsclient({
	baseUrl     : "127.0.0.1",
	port        : "8003", //8003 is the default web socket port for anyproxy
	onOpen : function(){
		console.log("connection stablished");
	},
	onGetUpdate : function(record){
		//get an updated record
		console.log(record);
	},
	onError     : function(e){
		console.log("an error occurred :" + e);
	},
	onClose     : function(e){
		console.log("connection closed");
	}
});

````