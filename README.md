# SpringCloudConfig

## Create Config Service Instance

```
cf create-service -c '{"git": { "uri": "https://github.com/phopper-pivotal/SpringCloudConfig/config-repo/", "label": "develop" } }' p-config-server standard config-server
```

If set incorrectly you can always issue a `update-serice` command once the config-server service instance is running. *THIS IS NOT TRUE, figure out why. for not delete and create with proper URI*

```
cf update-service -c '{"git": { "uri": "https://github.com/phopper-pivotal/SpringCloudConfig/config-repo/", "label": "develop" } }' config-server
Updating service instance config-server as phopper@pivotal.io...
FAILED
Server error, status code: 502, error code: 10001, message: The service broker rejected the request to https://spring-cloud-broker.cfapps.pez.pivotal.io/v2/service_instances/9a7dd543-d388-461c-a6d7-f3707236d573?accepts_incomplete=true. Status Code: 404 Not Found, Body:
```

```
cf update-service -c '{"git": { "uri": "https://github.com/phopper-pivotal/SpringCloudConfig/config-repo/", "label": "develop" } }' config-server
```


