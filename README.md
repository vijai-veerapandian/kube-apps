# Validate the apps internally from the kubernetes cluster itself.

# This creates a temporary pod and cleans it up when you exit.
kubectl run -it --rm --image=curlimages/curl:latest debug-pod -- sh

curl http://app1:<portnumber>
