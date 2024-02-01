# sitecontainers-sample
This repository contains sample sitecontainers app

You can either deploy just by clicking the button

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2Fappservice-linux-sidecar%2Fmain%2Fnginx-sample%2Farmtemplatemultictr.json" target="_blank">
<img src="https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/deploybutton.png"/>
</a>


Or you can run the commands below.

You can create a site with side cars using the arm template armtemplatemultictr.json -
 - az group create --name <RESOURCE_GROUP> --location <REGION>
 - az deployment group create --resource-group <RESOURCE_GROUP>  --parameters webAppName=<WEB_APP_NAME> sku=B1 --template-file armtemplatemultictr.json

Here is how you will see the app:
- <APP_URL> : Shows up Nginx home page from main Nginx container.
- <APP_URL>/dotnetcore : Shows up welcome page from dotnet sidecar container.
- <APP_URL>/python : Shows up welcome page from python sidecar container.
- <APP_URL>/nodejs : Shows up welcome page from nodejs sidecar container.

