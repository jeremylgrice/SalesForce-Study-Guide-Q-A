# SalesForce Study Guide
  <p align="center"><img src="https://user-images.githubusercontent.com/12513606/156643945-63967b38-5306-4461-9829-a20def922a76.png" /></p>

----
<h3>Knowledge Check: Salesforce Commerce API</h3>

| Question  | Answer  |
|---|---|
| Some of the core models are extendable and configurable through decorator pattern | True  |
| You are writing a mobile storefront application, and you need to implement the checkout using Commerce APIs. Which API will you use? | Shopper API |
| In order to connect Sample Apps to your sandbox, what are some of the parameters you need to set up in api.js? Select the 2 correct choices. | 1. SiteId, ClientId, RealmId, InstanceId. <br/> 2. SiteId, RealmId, InstanceId, ShortCode  |
| Where are allowed scopes configured for the Commerce API? | API Client in Account Manager |
| When do you use Shopper API over Management API? Select the 2 correct choices. | 1. When adding a product to a basket   2. When login a customer into the site|
| What are some of the reasons for adopting Headless Commerce? Select the 2 correct answers. | 1. It decouples the front end from the back end   2. It offers great flexibility to make changes |

----
<h3>Knowledge Check: Controllers</h3>

| Question  | Answer  |
|---|---|
| What file does this code refer to: `require('server');` | server.js in the modules/server folder |
| Which of the following statements is not correct? | A controller can invoke another controller |
| Which is not a method for extending a specific controller route (i.e. Home-Show) | Extend |
| If you extend a controller route, can you prepend as well as append to the same route? | True |
| If you remove `next();` on a route, what is the effect? | The next middleware function in the chain is not executed |
| Where can you find the methods of the response (res) attribute used in routes? For example, `res.render()` | Under SFRA / Server-side JS / Class: <a href="https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fsfrajsdoc%2Fjs%2Fserver%2Fmodules_server_response.js.html">Response documentation</a> |


----
<h3>Knowledge Check: ISML</h3>

| Question  | Answer  |
|---|---|
| The SFRA modules directory is a cartridge | False |
| The cartridge path controls the behavior of your site | True |
| Cartridges can only be uploaded using VSCode | False |
| Which one of these is considered a best practice? | Create your custom code in a cartridge, and put that cartridge in front of `app_storefront_base` in the cartridge path |
| If there are 2 code versions in your sandbox, which one is a true statement? | During execution, the cartridge path looks for cartridges in the active version |


----
<h3>Knowledge Check: Cartridges</h3>

| Question  | Answer  |
|---|---|
| | |
| | |
| | |
| | |
