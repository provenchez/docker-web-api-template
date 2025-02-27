# docker-web-api-template

docker build -t web-api-image .

docker run --hostname=bfe8b1789ac1 --env=PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin --env=APP_UID=1654 --env=ASPNETCORE_HTTP_PORTS=80 --env=DOTNET_RUNNING_IN_CONTAINER=true --env=DOTNET_VERSION=8.0.7 --env=ASPNET_VERSION=8.0.7 --network=bridge --workdir=/API --restart=no --runtime=runc -p 5001:80 -d web-api-image

open http://localhost:5001/weatherforecast