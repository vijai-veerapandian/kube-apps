# Validate the apps internally from the kubernetes cluster itself.

# This creates a temporary pod and cleans it up when you exit.
kubectl run -it --rm --image=curlimages/curl:latest debug-pod -- sh

Command to check the url from the temp pod container
curl http://app1:<portnumber>
