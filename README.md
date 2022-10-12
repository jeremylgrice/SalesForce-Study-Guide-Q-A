
# SalesForce Study Guide
  <p align="center"><img src="https://user-images.githubusercontent.com/12513606/156643945-63967b38-5306-4461-9829-a20def922a76.png" /></p>
  
  <p align="center">This is a generalized study guide with questions taken from the Trailheads fast path knowledge checks. This is in no way associated with Salesforce, and was created to help myself and possibly others pass the certification exam.</p>
  
  
<details>
  <summary>Important links</summary>
  
  <br />

  | Description | Link |
  |---|---|
  | Official Documentation (new) | https://developer.salesforce.com/docs/?search_text=post%20action%20link |
  | Official Documentation (old) | https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsptopic=%2Fcom.demandware.dochelp%2Fcontent%2Fb2c_commerce%2Ftopics%2Fsite_development%2Fb2c_business_manager_extension_points.html |

  <br />

</details>

<details>
    <summary>Overview</summary>
  
    The following will be various questions I have compiled while studying for the certification test.

  </details>

  <details>
  <summary>Knowledge Check: Misc.</summary>

  <br />

  | Question  | Choices | Answer  |
  |---|---|---|
  | Question - Where would apple pay be disabled for a site? Payment methods, payment processor, or apple pay |  | <details><summary>Reveal Answer</summary>Payment Method</details>  |
  | Question - Which product types are there in SFCC ? |  | <details><summary>Reveal Answer</summary>Standard, base(master), variation group, variation product, product set, product bundle.</details>  |  |
  | Question - What is the correct syntax to define hooks in package.json file in order to configure functionality to be called at a specific point in your application flow or at a specific event? |  | { "hooks": "./cartridge/scripts/hooks.json" } |
  | Question - How would you make a variable be persistent during multiple pages for your current Site? |  | <isset name="var" scope="session"> |
  | Question - What would be the expected cache policy for a page that is rendered by another page where its controller has defined cache.applyDefaultCache in its middleware chain? |  | If this page is rendered by another controller with another cache configuration it would overwrite the previous one |
  | Question - Cache for stored pages are only invalidated and a new one pulled from the applications server when |  | The defined caching time is exceeded or a replication is performed, or the merchant triggers an explicit page cache invalidation in Business Manager. |
  | Question - What happens if the log size limit is reached? |  | Logging is suspended until the next day |
  | Question - A storefront user is trying to submit a form, but nothing is happening and data is not submitted. What is the reason? | a. `No action attribute` <br><br> b. `Validation Failing` <br><br> c. `CSRF validation failed` <br><br> d. `The transaction failed on the controller action` <br><br> e. `all answers are correct` | <details><summary>Reveal answer</summary>All answers are correct</details> |
  | Question - File types accepted to import data in a sandbox instance? Choose all answers that apply. | a. `JSON` <br><br> b. `CSV` <br><br> c. `XML` <br><br> d. `YAML` <br><br> d. `B and C are correct` | <details><summary>Reveal answer</summary> d. B and C are correct</details> |
  | Question - Select the correct syntax about how to use <isprint> tag. | a. `<isprint value="${pdict.numbers}" style="INT" />` <br><br> b. `<isprint value="${pdict.numbers}" />` <br><br> c. `<isprint value="${pdict.numbers}" encoding="false" />` <br><br> d. `<isprint value="${pdict.numbers}" formater="INTEGER" />` | <details><summary>Reveal answer</summary> the answer is b </details> |
  | Question - Given this piece of code, how can you access it inside the loop? `<isloop items="${pdict.listOfItems}" status="status" var="variable">` | a. `${pdict.variable}` <br><br> b. `${status}` <br><br> c. `${variable}` <br><br> d. `${listOfItems[status.index]}` | <details><summary>Reveal answer</summary> c. #{variable} </details> |
  | Question - What is the purpose of the `<isif>` tag? | a. `Anything enclosed in an <isif>... </isif> structure isn't parsed by the template processor and doesn't appear in the generated storefront page.` <br><br>  b. `With <isif> you can loop through the elements of a specified iterator.` <br><br> c. `The <isif> tag outputs the result of expressions and template variables` <br><br> d. `The <isif> tag group lets you create conditional programming constructs using custom tags` | <details><summary>Reveal answer</summary> d. The `<isif>` tag group lets you create conditional programming constructs using custom tags </details> |
  | Question - Select ISML tag or tags that allows you to reuse code in your templates | a. `<isinclude>` <br><br> b. `<isloop>` <br><br> c. `<isdecorate>` <br><br> d. `<iscontent>` <br><br> e. `A and D are correct` <br><br> f. `A and C are correct` | <details><summary>Reveal answer</summary> f. A and C are correct </details> |
  | Question - What salesforce tag is the best way to debug on ISML? | a. `<ismodule>` <br><br> b. `<isdebug>` <br><br> c. `<iscontent>` <br><br> d. `<isprint>` | <details><summary>Reveal answer</summary> d. `<isprint>` </details> |
  | Question - Inside a job flow… how can you set it up so that a job step returns a flag to be used by next job steps? | a. On BM, enable exit status rules <br><br> b. Create script with `return new Status(Status.OK);` <br><br> c. Create script with `return new StatusFlag(Status.OK);` <br><br> d. Create script with `return new Status(Status.OK, 'OK');` <br><br> e. B and D are correct | <details><summary>Reveal answer</summary> e. B and D are correct </details> |
  | For your current site you have multiple locales defined. You’re checking PDP in order to check product description. What happens when a certain locale is not found? | a. `No description is shown` <br><br> b. `Error message is shown` <br><br> c. `Description is shown in fallback locale if configured` <br><br> d. `A and C are both correct` | <details><summary>Reveal answer</summary> d. A and C are both correct. </details> |
  | What is the best way of making use of CSRF Tokens in your templates? | a. `Add a <isscript> tag in ISML to generate that token` <br><br> b. `Add the snippet csrfProtection.generateToken as middleware in your controller` <br><br> c. `Require the CSRFProtection class in the controller and send the token that calls generateToken() via the viewData` <br><br> d. `Business Manager will protect your ecommerce site against CSRF attacks. No action is needed` | <details><summary>Reveal answer</summary> b. Add the snippet csrfProtection.generateToken as middleware in your controller </details> |
  | Best practice about how you should restrict access to a certain page only for logged users? | a. `Checkiong customer.authenticated property and rendering new template if false` <br><br> b. `Checking session.userAuthenticated property and rendering new template if true` <br><br> c. `Adding userLoggedIn.validateLoggedIn in controller middleware chain` <br><br> d. `Checking customer.userAuthenticated property and rendering new template if false` | <details><summary>Reveal answer</summary> c. Adding `userLoggedIn.validateLoggedIn` in `controller.middleware` chain </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  | Question | Choices | <details><summary>Reveal answer</summary> answer here </details> |
  
  <br />
</details>

<details>
  <summary>Knowledge Check: Salesforce Commerce API</summary>

  <br />
  
  | Question  | Answer  |
  |---|---|
  | Some of the core models are extendable and configurable through decorator pattern | True  |
  | You are writing a mobile storefront application, and you need to implement the checkout using Commerce APIs. Which API will you use? | Shopper API |
  | In order to connect Sample Apps to your sandbox, what are some of the parameters you need to set up in api.js? Select the 2 correct choices. | 1. SiteId, ClientId, RealmId, InstanceId. <br/> 2. SiteId, RealmId, InstanceId, ShortCode  |
  | Where are allowed scopes configured for the Commerce API? | API Client in Account Manager |
  | When do you use Shopper API over Management API? Select the 2 correct choices. | 1. When adding a product to a basket <br /> 2. When login a customer into the site|
  | What are some of the reasons for adopting Headless Commerce? Select the 2 correct answers. | 1. It decouples the front end from the back end <br /> 2. It offers great flexibility to make changes |

  <br />
</details>

<details>
<summary>Knowledge Check: Controllers</summary>

  <br />
  
| Question  | Answer  |
|---|---|
| What file does this code refer to: `require('server');` | server.js in the modules/server folder</details> |
| Which of the following statements is not correct? | A controller can invoke another controller</details> |
| Which is not a method for extending a specific controller route (i.e. Home-Show) | Extend |
| If you extend a controller route, can you prepend as well as append to the same route? | True |
| If you remove `next();` on a route, what is the effect? | The next middleware function in the chain is not executed |
| Where can you find the methods of the response (res) attribute used in routes? For example, `res.render()` | Under SFRA / Server-side JS / Class: <a href="https://documentation.b2c.commercecloud.salesforce.com/DOC1/index.jsp?topic=%2Fcom.demandware.dochelp%2Fsfrajsdoc%2Fjs%2Fserver%2Fmodules_server_response.js.html">Response documentation</a> |
  
  <br />
</details>

<details>
  <summary>Knowledge Check: ISML</summary>

  <br />
  
  | Question  | Answer  |
  |---|---|
  | The SFRA modules directory is a cartridge | False |
  | The cartridge path controls the behavior of your site | True |
  | Cartridges can only be uploaded using VSCode | False |
  | Which one of these is considered a best practice? | Create your custom code in a cartridge, and put that cartridge in front of `app_storefront_base` in the cartridge path |
  | If there are 2 code versions in your sandbox, which one is a true statement? | During execution, the cartridge path looks for cartridges in the active version  |

</details>

<details>
  <summary>Knowledge Check: Cartridges</summary>

  <br />
  
  | Question  | Answer  |
  |---|---|
  | The SFRA modules directory is a cartridge | False |
  | The cartridge path controls the behavior of your site | True |
  | Cartridges can only be uploaded using VSCode | False |
  | Which one of these is considered a best practice? | Create your custom code in a cartridge, and put that cartridge in front of app_storefront_base in the cartridge path |
  
</details>

<details>
  <summary>Knowledge Check: Transactions and SFRA Middleware Events</summary>
  
  <br />

  | Question  | Answer  |
  |---|---|
  | _____ allow you to extend the data model to store custom data? | Custom Objects  |
  | What are two ways to create a custom object definition in Business Manager? | 1. Manually define all fields <br /> 2. Import a custom object definition metadata file  |
  | What do you need to save any persistent system or custom object? | Transactions |
  | It’s the best practice to log informational messages and warnings that could happen during the normal execution of your code? | True |
  | The Log Center allows you to filter logs by what two filters? | 1. Severity <br /> 2. Category |
  | To make sure your transaction is the last thing that gets handled by the Handler route, use the ______ event? | `route.beforeComplete` |
  | What kind of hook is a newer REST API offered by Salesforce? | OCAPI Hook |
  | What is another name for a Custom Hook? | SFRA Hook |
  | What do you use to configure functionality to be called at a specific point in your application flow or at a specific event? | Hooks |
  | What is an example of extension_point_name? | dw.order.calculate |

  <br />
</details>
  
<details>
  <summary>Knowledge Check: Job Framework</summary>
  
  <br />

  | Question  | Answer  |
  |---|---|
  | The job framework allows the platform to perform processes for integration purposes | True  |
  | What are two integration processes that the jobs framework allows the platform to perform? | 1. Import products and prices from a PIM <br /> 2. Export custom objects and clean up after export  |
  | As part of the customer agreement, there is a max limit of data usage. What happens when a customer goes over those limits? | It generates an overage charge |
  | Schedules only work in PIG instances so you must run manually in sandboxes | True |
  | Where do export files go? | IMPEX dir |

  <br />
</details>

