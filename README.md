# DirectIQ Rest API Document

Welcome to the DirectIQ REST API document. You can use our API to access DirectIQ data endpoints to read/write objects like contacts, campaigns, templates and more.

We have language bindings in Shell and C#.

## Getting Started

To connect to the API with basic auth you need the following:

* Secure URL pointing to DirectIQ REST API endpoint
* Username of DirectIQ account
* API key for the user

## Authentication

An important part of authentication is your API key. You can access your API key from **My Account > Social Media & Integrations > API Integration** in your DirectIQ dashboard.

If you are not a registered DirectIQ user,[you can register here](https://www.directiq.com)

## Example with cURL

### Unix style

```shell
curl -X GET \
     https://restapi.directiq.com/contactlists \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key"
```

You can simply check if authentication is working with cURL command. Make sure to replace _your-api-key_ with your real API key, and _your-user-name_ with your real DirectIQ user name.

**Note:** Backslash ("\\") at the end of each line helps you paste your cURL command with multiple lines in Unix-like operating system shells (Mac OS for example). In Windows, you can use the caret character ("^") instead of "\\" for multine cURL command.

### Windows style

```shell
curl -X GET ^
     https://restapi.directiq.com/contactlists ^
     -H "user-name: your-user-name" ^
     -H "api-key: your-api-key"
```

## Example with C#

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");
var request = new RestRequest("contactlists", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

## Support

if you need any help or have any questions, please send an email to [support@directiq.com](mailto:support@directiq.com).

## Reference
