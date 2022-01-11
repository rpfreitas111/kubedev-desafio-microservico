FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /app
COPY /Review.Web/*.csproj ./
RUN dotnet restore 

COPY /Review.Web/ .
RUN dotnet publish -c Release -o /app/publish

FROM mcr.microsoft.com/dotnet/aspnet:5.0
ARG ASPNETCORE_URLS
ENV ASPNETCORE_URLS=http://+:8282
WORKDIR /app
COPY --from=build /app/publish .
EXPOSE 8282
ENTRYPOINT [ "dotnet", "Review.Web.dll" ]
