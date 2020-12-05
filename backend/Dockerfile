FROM mcr.microsoft.com/dotnet/core/sdk:3.1.402-buster
COPY . /app
WORKDIR /app/src/Conduit
RUN ["dotnet", "restore"]
RUN ["dotnet", "build"]
EXPOSE 5000
RUN chmod +x ./entrypoint.sh
CMD /bin/bash ./entrypoint.sh