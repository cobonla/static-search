# StaticSearch

StaticSearch is object, It provide methods to client call to server to get data. The technology used is ajax.

**Platform**
- Jquery

**Usage**

Import file static-search.js (using ES6) or static-search.ie.js (for old browsers) to your html page. Then create new object and run it.

```
var search = new StaticSearch({
	url: "Default get from attribute action of form",
	method: "Default get from attribute method of form",
	dataType: "html",
	autoload: true,
	
	// Setting elements in your html page
	elements: {
		form: ".ss-form",
		pagination: ".ss-pagination a",
		order: ".ss-order span",
		record: ".ss-record a",
		success: ".ss-success",
		error: ".ss-error"
	},
	
	// Setting custom method
	methods: {
		render: {
			error: function(){},
			success: function(){}, 
		}
	},
	
	// Setting custom events
	events: {
		submit: function(){},
		loading: function(){},
		loaded: function(){},
		render: function(){},
		rendered: function(){}
	}
});
```

Then call run to apply to.

```
search.run();
```

OK, now it working!
