# WC-API-JS-Client

Add a reference to your index.html file

`<script src="wcapi.js"></script>`

`<script src="services.js"></script>`

##### Do not forget to add your `store URL`, `consumer key` and `consumer secret` to the _services.js_ file. 

Inject the `WP` service in your controllers.

```javascript
app.controller('myCtrl', function($scope, WP){
  var Woocommerce = WP.WP();
  
  Woocommerce.get('products/categories', function(err, data, res){
    if(err)
      console.log(err);
    console.log(JSON.parse(res));
  })
});
```

**You may need to change the Module Name accordingly in the services.js file.**
  
*Works like a Charm in Ionic and AngularJS apps.*
_For more endpoints check the documentation at [https://github.com/woothemes/wc-api-node](https://github.com/woothemes/wc-api-node "WC NODE API")_

