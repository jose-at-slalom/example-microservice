# Example Microservice

## Running Locally

Execute this command: `dotnet run`

## Running Using Podman

First build the image.
```
podman build --tag examplemicroservice -f Dockerfile
```

Then run the image.
```
podman run -it --rm -p 3000:80 --name examplecontainer examplemicroservice
```
