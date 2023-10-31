# Example Microservice

An example microservice written in C# following [this tutorial](https://dotnet.microsoft.com/en-us/learn/aspnet/microservice-tutorial/intro).

## Running Locally

Execute this command to run the service locally. 
```
dotnet run
```

Then access the JSON response by pointing to this URL: `http://localhost:3000/WeatherForecast`

Or execute a cURL command:
```
curl -s -X GET "http://localhost:3000/WeatherForecast"
```

## Running Using Podman

First build the image.
```
podman build --tag examplemicroservice -f Dockerfile
```

Then run the image.
```
podman run -it --rm -p 3000:80 --name examplecontainer examplemicroservice
```
