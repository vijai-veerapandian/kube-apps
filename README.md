### Validate the apps internally from the kubernetes cluster itself.

1. Create a temporary pod with network tools. It will be removed when you exit.
```
kubectl run -it --rm --image=curlimages/curl:latest debug-pod -- sh
```
 2. From inside the debug pod's shell, use curl to test the internal services.

### Test audiobookshelf (app1)
 The service is named 'audiobookshelf' in the 'audiobookshelf' namespace, on port 3005.
```
curl http://audiobookshelf.audiobookshelf:3005
```

### Test myweather-app (app2)
 The backend service is named 'backend' in the 'myweather-app' namespace, on port 5000.
```
curl http://backend.myweather-app:5000
```

 The frontend service is named 'frontend' in the 'myweather-app' namespace, on port 9090.
```
curl http://frontend.myweather-app:9090
```