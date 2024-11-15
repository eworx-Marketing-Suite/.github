# Welcome to eworx Marketing Suite Examples

The eworx Marketing Suite (eMS) provides its own API for connecting to other systems.
In this project we provide examples in different programming languages ​​to illustrate the application.

The complete API documentation can be found at https://www.eworx.at/doku/api-schnittstellenbeschreibung/ (Documentation in German)

We provide the following programming languages
1. [visit C# examples](../../../../CSharp-API-Demo-Project)
2. [visit PHP examples](../../../../Php-API-Demo-Project)
3. [visit Node.js examples](../../../../NodeJS-API-Demo-Project)

## Common required setup

In order to use the API, an application must first be registered, in which a selection of methods is made that are to be used. The name given there is required for logging into the eMS.  

Register your application at https://www.eworx.at/doku/api-schnittstellenbeschreibung/#zugang-zur-api-anlegen.

The connection to the eMS is ensured with a ServiceAgent, which is created at the beginning of each use case.
