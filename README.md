# Vulnerable Advertisement API

## Description
Application is a set of APIs that create advertising. The application supports the following functionality:
1. Creating/updating/deleting ads. For each ad it should be specified product and channel.
1. Manager works with ads for specified product (is controlled by role). Manager can also see the list of all channels and products.
1. Visitor can see only the ad that is currently running. The passed ad and future ad is not available for him.
1. Visitor isn't logged in the application and doesn't have session token.
1. Creating/updating/deleting ad products. One can also view list of all products and product details
1. Creating/updating/deleting ad channels. One can also view list of all channels and channel details
1. The same operations are available for users. User management is performed by admin.
1. There are three different user roles in the application:
    * Visitors, who can view currently running ad
    * Managers who create ad for specific products. Managers don't have access to other user's information.
    * Admin. Can view/update/delete ads created by different users. In addition, is able to create/update/delete products and channels. Can create/update/delete users.


## Prerequisites
* Microsoft Windows 7 or higher
* [Microsoft SQL Server 2017 Express Edition](https://www.microsoft.com/en-us/download/details.aspx?id=55994) or higher
* [Microsoft SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017)
* [Microsoft .NET Core 2.2 Runtime](https://dotnet.microsoft.com/download) or higher
* [Microsoft Internet Information Services](https://www.itnota.com/install-iis-windows/)
* [Postman](https://www.getpostman.com/)
* [OWASP ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project)
* Any browser plugin to work with cookies

## How to
* [Restore a Database Backup Using SSMS](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)
* [Create a Database User](https://docs.microsoft.com/en-us/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)
* [Host ASP.NET Core on Windows with IIS](https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-2.2)

## Repository Contents
* API.zip - API web application. Inside archive: 
  * appsettings.json - Main configuration file. Setup connection to database
  * web.config - Web application configuration file. Application start configuration (no changes required)
* Postman.json - Postman requests collection with API tests. Please, look through it to understand what APIs project has. The link to the working APIs may change.
* Database.bak - SQL database backup with test data

## Test data
### Admin: 
* Login = Admin, password = admin
### Manager role:
* Login = Samsung Galaxy Note Manager, password = samsung
* Login = Apple iPhone Manager, password = apple
* Login = Microsoft Surface Manager, password = Microsoft
### Visitor role:
* Login = Visitor 1 (or 2/3/4), password = new_pass
