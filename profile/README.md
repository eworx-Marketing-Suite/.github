# Welcome to eworx Marketing Suite Examples

The eworx Marketing Suite (eMS) provides its own API for connecting to other systems.
In this project we provide examples in different programming languages ​​to illustrate the application.

The complete API documentation can be found at https://www.eworx.at/doku/api-schnittstellenbeschreibung/ (Documentation in German)

We provide the following programming languages
1. visit C# examples
2. visit PHP examples

## Common required setup

In order to use the API, an application must first be registered, in which a selection of methods is made that are to be used. The name given there is required for logging into the eMS.  

Register your application at https://www.eworx.at/doku/api-schnittstellenbeschreibung/#zugang-zur-api-anlegen.

The connection to the eMS is ensured with a ServiceAgent, which is created at the beginning of each use case.

```cs
// C# demo code to create an eMS ServiceAgent
EmsServiceAgent serviceAgent = new EmsServiceAgent()
    .UseServiceUrl("")     // not required, default value "https://mailworx.marketingsuite.info/services/serviceagent.asmx"
    .UseLanguage("EN")     // Language of the text values ​​returned
    .UseCredentials(
        "[Account]",        // account name (Mandant) of the eMS to login
        "[Username]",       // user name to use to login
        "[Password]",       // the user's password
        "[Application]"     // the name of the registered application
    );
```
