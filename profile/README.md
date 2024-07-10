# Welcome to eworx Marketing Suite Examples

The eworx Marketing Suite (eMS) provides its own API for connecting to other systems.
In this project we provide examples in different programming languages ​​to illustrate the application.

The complete API documentation can be found at https://www.eworx.at/doku/api-schnittstellenbeschreibung/ (Documentation in German)

We provide the following programming languages
1. [visit C# examples](../../../../CSharp-API-Demo-Project)
2. visit PHP examples (in work)

## Common required setup

In order to use the API, an application must first be registered, in which a selection of methods is made that are to be used. The name given there is required for logging into the eMS.  

Register your application at https://www.eworx.at/doku/api-schnittstellenbeschreibung/#zugang-zur-api-anlegen.

The connection to the eMS is ensured with a ServiceAgent, which is created at the beginning of each use case.

##### C# for EmsServiceAgent and create a simple request
```cs
// C# demo code to create an eMS ServiceAgent
EmsServiceAgent serviceAgent = new EmsServiceAgent()
    .UseServiceUrl("https://mailworx.marketingsuite.info/services/serviceagent.asmx")
                    // Url to the eMS service.
                    // Not required, default value "https://mailworx.marketingsuite.info/services/serviceagent.asmx"
    .UseLanguage("EN")     // Language of the text values ​​returned. Not required, default value is "EN"
    .UseCredentials(
        "[Account]",        // account name (Mandant) of the eMS to login
        "[Username]",       // user name to use to login
        "[Password]",       // the user's password
        "[Application]"     // the name of the registered application
    );

// create simple request
serviceAgent.CreateRequest(new CampaignsRequest());
```

##### PHP for EmsServiceAgent and create a simple request
```php
// php demo code to create an eMS ServiceAgent
$serviceAgent = new \eMS\EmsServiceAgent()
    .useServiceUrl("https://mailworx.marketingsuite.info/Services/JSON/ServiceAgent.svc")
                    // Url to the eMS service.
                    // Not required, default value "https://mailworx.marketingsuite.info/Services/JSON/ServiceAgent.svc"
    .useLanguage("EN")     // Language of the text values ​​returned. Not required, default value is "EN"
    .useCredentials(
        "[Account]",        // account name (Mandant) of the eMS to login
        "[Username]",       // user name to use to login
        "[Password]",       // the user's password
        "[Application]"     // the name of the registered application
    );

// create simple request
$serviceAgent.createRequest('GetCampaigns');
```
