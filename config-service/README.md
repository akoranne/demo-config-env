# Config Service

This app shows example of the config service.

It is using the following config repo `https://github.com/akoranne/configs`, 
specially `a-bootiful-client.properties`. 


## Local Build & Test
1. Build the project
	```
	$> ./mnvw clean package
	```

2. Run the project locally
	```
	$> ./mnvw spring-boot:run
	```

3. Test locally
	```
	Go to http://localhost:8888/a-bootiful-client/default
	 
	You should see the jason document.
	```

## Cloud 
1. Push to PCF
	```
	$> cf push
	```

2. Test locally
	```
	Go to
		http://config-service.apps.<pcf-domain>/a-bootiful-client/default
	
	For example
		http://config-service.apps.lab02.den.ecsteam.io/a-bootiful-client/default
	 
	You should see the jason document.
	```


## Results
```
{
	"name": "a-bootiful-client",
	"profiles": [
		"default"
	],
	"label": "master",
	"version": "144c56b57dba65179bf4f7be8765fcdb0f9260a0",
	"state": null,
	"propertySources": [
		{
			"name": "https://github.com/akoranne/configs.git/a-bootiful-client.properties",
			"source": {
				"user": "joe@acme.com",
				"password": "abc123",
				"message": "Hello World from Humpty Dumpty"
			}
		}
	]
}
```
