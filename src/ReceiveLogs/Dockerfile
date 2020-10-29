#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster AS build
WORKDIR /src

COPY ["ReceiveLogs.csproj", "ReceiveLogs/"]
RUN dotnet restore "ReceiveLogs/ReceiveLogs.csproj"
COPY . .

FROM build AS publish
RUN dotnet publish "ReceiveLogs.csproj" -c Release -o /app/publish

FROM mcr.microsoft.com/dotnet/core/runtime:3.1 AS base
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet","ReceiveLogs.dll"]