# API

**Auth service (:8181)**
- register new user
- login (creates new session id)
- auth login user (validates existing session id)
- logout (invalidates existing session)

**User Service (:8080)**
- get current user info (requires login)
- get user info  (requires login)
- edit user (requires login and same user id)
- delete user (requires login and same user id)
- get all users (requires login)

# Deployment
- this applies postgres and secrets
```
kubectl apply -f .
```
 - this applies manifests for main app
```
cd app
kubectl apply -f .
```
 - this applies manifests for auth app
```
cd ..
cd auth
kubectl apply -f .
```
```
minikube addons enable ingress
```