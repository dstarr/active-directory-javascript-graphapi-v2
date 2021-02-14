---
page_type: sample
languages:
- javascript
- html
products:
- microsoft-identity-platform
- azure-active-directory-v2
- ms-graph
description: "A simple JavaScript single-page application calling Microsoft Graph API using msal.js (w/ AAD v2 endpoint)"
urlFragment: "active-directory-javascript-graphapi-v2"
---

# MSAL JavaScript Single-page Application using Implicit Flow

A simple vanilla JavaScript single-page application which demonstrates how to configure [MSAL.JS Core](https://www.npmjs.com/package/msal) to login, logout, protect a route, and acquire an access token for a protected resource such as [Microsoft Graph API](https://docs.microsoft.com/en-us/graph/overview).

**Note:** A quickstart guide covering this sample can be found [here](https://docs.microsoft.com/azure/active-directory/develop/quickstart-v2-javascript).

**Note:** A more detailed tutorial covering this sample can be found [here](https://docs.microsoft.com/azure/active-directory/develop/tutorial-v2-javascript-spa).

## Contents

| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `AppCreationScripts` | Contains automation scripts for Powershell users (can be safely removed if desired). |
| `JavaScriptSPA`   | Contains sample source files.              |
| `authPopup.js`    | Main authentication logic resides here (using Popup flow). |
| `authRedirect.js` | Use this instead of `authPopup.js` for authentication with redirect flow. |
| `authConfig.js`   | Contains configuration parameters for the sample. |
| `graph.js`        | Provides a helper function for calling MS Graph API. |
| `graphConfig.js`  | Contains API endpoints for MS Graph.       |
| `ui.js`           | Contains UI logic.                         |
| `index.html`      |  Contains the UI of the sample.            |
| `.gitignore`      | Defines what to ignore at commit time.     |
| `CHANGELOG.md`    | List of changes to the sample.             |
| `CODE_OF_CONDUCT.md` | Code of Conduct information.            |
| `CONTRIBUTING.md` | Guidelines for contributing to the sample. |
| `LICENSE`         | The license for the sample.                |
| `package.json`    | Package manifest for npm.                  |
| `README.md`       | This README file.                          |
| `SECURITY.md`     | Security disclosures.                      |
| `server.js`       | Implements a simple Node server to serve index.html.  |

## Prerequisites

- [Node.js](https://nodejs.org/en/) must be installed to run this sample.
- A modern web browser. This sample uses **ES6** conventions and will not run on **Internet Explorer**. See [here](https://github.com/AzureAD/microsoft-authentication-library-for-js/tree/dev/samples/msal-core-samples/VanillaJSTestApp/app/ie11-sample) for an IE11-compatibility.

## Setup

1. [Register a new application](https://docs.microsoft.com/azure/active-directory/develop/scenario-spa-app-registration) in the [Azure Portal](https://portal.azure.com). Ensure that the application is enabled for the [implicit flow](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-implicit-grant-flow).
2. Open the [/JavaScriptSPA/authConfig.js](./JavaScriptSPA/authConfig.js) file and provide the required configuration values.

## Running the sample

1. Configure authentication and authorization parameters:
   1. Open `authConfig.js`
   2. set the `clientId` parameter to your app/client ID from the AAD Portal.
1. Open a terminal in the root project directory.
   1. Run `npm install` to get all dependencies.
   1. Run `npm start` to start the web server.
1. Finally, open a browser to [http://localhost:3000](http://localhost:3000).

> How did we do? Consider [sharing your experience with us](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR73pcsbpbxNJuZCMKN0lURpUQktGUlJTSjdEWkYzWjRKTlRTUFNYUDlFViQlQCN0PWcu).

## Key points

This sample demonstrates the following MSAL workflows:

* How to configure application parameters.
* How to sign-in with popup and redirect methods.
* How to sign-out.
* How to get user consent incrementally.
* How to acquire an access token.
* How to make an API call with the access token.

## Contributing

If you'd like to contribute to this sample, see [CONTRIBUTING.MD](./CONTRIBUTING.md).

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
