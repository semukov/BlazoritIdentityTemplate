# BlazoritIdentityTemplate
## Blazor (WebAssembly ASP.NET Core hosted) production template by JWT authentication and authorization using storage PostgreSQL
![alt text](https://github.com/semukov/BlazoritIdentityTemplate/blob/master/BlazoritIdentityTemplate.png)

##### At the beginning, you need add file "appsettings.json" in this template solution in folder /Blazorit/app/Server/appsettings.json.
You have to add this code to the file /Blazorit/app/Server/appsettings.json:
```
{
  "ConnectionStrings": {
    "DefaultConnection": "server=server_address;Port=5432; Database=db_name; Username=user_name; Password=pass"
  },
  "AppSettings": {
    "SecurityKey": "some long secret key"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```
You have to change DefaultConnection string for your Database. Also, you can change SecurityKey in this file.

Then, you need run command for migrations to your db: 
```
dotnet ef database update
```

If you want to use docker for PostgreSQL and your app, then look into DevOps folder and run docker-compose.yml file:
```
docker-compose up -d
```
