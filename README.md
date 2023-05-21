# csharp-website-with-docker
A template to use for making websites in C# and deploying to Docker.

https://docs.docker.com/language/dotnet/
Updated for dotnet 7.0
mkdir dotnet-docker
cd dotnet-docker
dotnet new webapp -n myWebApp -o src --no-https
dotnet run --urls http://localhost:5000
docker build --tag dotnet-docker .
docker run dotnet-docker
docker run --publish 5000:80 dotnet-docker