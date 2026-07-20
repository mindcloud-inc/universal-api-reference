# <img src="https://images.mindcloud.co/apps/icons/sage-sales-management-icon-square_1776171352713.png" alt="Sage Sales Management logo" width="28" height="28"> Sage Sales Management: Universal API

Sage Sales Management is Sage's CRM and field sales platform for managing accounts, contacts, opportunities, activities, products, orders, users, and related operational data through the official REST API v4.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sageSalesManagement/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 129
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.forcemanager.com/
- **Vendor API docs:** https://developer.forcemanager.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (129)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates an account in Sage Sales Management. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an account from Sage Sales Management. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Sage Sales Management. |
| [Get Account Address](actions/get-account-address.md) | GET | Retrieves an account address from Sage Sales Management. |
| [Get Account Addresses Schema](actions/get-account-addresses-schema.md) | GET | Retrieves the account addresses schema from Sage Sales Management. |
| [Get Account Segments Schema](actions/get-account-segments-schema.md) | GET | Retrieves the account segments schema from Sage Sales Management. |
| [Get Account Statuses Schema](actions/get-account-statuses-schema.md) | GET | Retrieves the account statuses schema from Sage Sales Management. |
| [Get Account Types Schema](actions/get-account-types-schema.md) | GET | Retrieves the account types schema from Sage Sales Management. |
| [Get Accounts Schema](actions/get-accounts-schema.md) | GET | Retrieves the accounts schema from Sage Sales Management. |
| [Get Branch](actions/get-branch.md) | GET | Retrieves a branch from Sage Sales Management. |
| [Get Branches Schema](actions/get-branches-schema.md) | GET | Retrieves the branches schema from Sage Sales Management. |
| [Get Countries Schema](actions/get-countries-schema.md) | GET | Retrieves the countries schema from Sage Sales Management. |
| [Get Currencies Schema](actions/get-currencies-schema.md) | GET | Retrieves the currencies schema from Sage Sales Management. |
| [Get Related Account](actions/get-related-account.md) | GET | Retrieves a related account from Sage Sales Management. |
| [Get Related Account Type](actions/get-related-account-type.md) | GET | Retrieves a related account type from Sage Sales Management. |
| [Get Related Account Types Schema](actions/get-related-account-types-schema.md) | GET | Retrieves the related account types schema from Sage Sales Management. |
| [Get Related Accounts Schema](actions/get-related-accounts-schema.md) | GET | Retrieves the related accounts schema from Sage Sales Management. |
| [List Account Addresses](actions/list-account-addresses.md) | GET | Retrieves account addresses from Sage Sales Management. |
| [List Account Segments](actions/list-account-segments.md) | GET | Retrieves account segments from Sage Sales Management. |
| [List Account Statuses](actions/list-account-statuses.md) | GET | Retrieves account statuses from Sage Sales Management. |
| [List Account Types](actions/list-account-types.md) | GET | Retrieves account types from Sage Sales Management. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Sage Sales Management. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from Sage Sales Management. |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Sage Sales Management. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Sage Sales Management. |
| [List Related Account Types](actions/list-related-account-types.md) | GET | Retrieves related account types from Sage Sales Management. |
| [List Related Accounts](actions/list-related-accounts.md) | GET | Retrieves related accounts from Sage Sales Management. |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zones from Sage Sales Management. |
| [Update Account](actions/update-account.md) | PUT | Updates an account in Sage Sales Management. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Sage Sales Management. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Sage Sales Management. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Sage Sales Management. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Sage Sales Management. |
| [Get Contact Types Schema](actions/get-contact-types-schema.md) | GET | Retrieves the contact types schema from Sage Sales Management. |
| [Get Contacts Schema](actions/get-contacts-schema.md) | GET | Retrieves the contacts schema from Sage Sales Management. |
| [Get Email](actions/get-email.md) | GET | Retrieves an email from Sage Sales Management. |
| [Get Emails Schema](actions/get-emails-schema.md) | GET | Retrieves the emails schema from Sage Sales Management. |
| [Get Entity Contacts Schema](actions/get-entity-contacts-schema.md) | GET | Retrieves the entity contacts schema from Sage Sales Management. |
| [Get Resources](actions/get-resources.md) | GET | Retrieves a resources from Sage Sales Management. |
| [Get Resources by Phone Number](actions/get-resources-by-phone-number.md) | GET | Finds resources in Sage Sales Management by phone number. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Sage Sales Management. |
| [List Contact Types](actions/list-contact-types.md) | GET | Retrieves contact types from Sage Sales Management. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Sage Sales Management. |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails from Sage Sales Management. |
| [List Entity Contacts](actions/list-entity-contacts.md) | GET | Retrieves entity contacts from Sage Sales Management. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Sage Sales Management. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates an opportunity in Sage Sales Management. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an opportunity from Sage Sales Management. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Sage Sales Management. |
| [Get Campaign Question](actions/get-campaign-question.md) | GET | Retrieves a campaign question from Sage Sales Management. |
| [Get Opportunities Schema](actions/get-opportunities-schema.md) | GET | Retrieves the opportunities schema from Sage Sales Management. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from Sage Sales Management. |
| [Get Opportunity Statuses Schema](actions/get-opportunity-statuses-schema.md) | GET | Retrieves the opportunity statuses schema from Sage Sales Management. |
| [Get Opportunity Types Schema](actions/get-opportunity-types-schema.md) | GET | Retrieves the opportunity types schema from Sage Sales Management. |
| [Get Sale](actions/get-sale.md) | GET | Retrieves a sale from Sage Sales Management. |
| [Get Sales Schema](actions/get-sales-schema.md) | GET | Retrieves the sales schema from Sage Sales Management. |
| [List Campaign Questions](actions/list-campaign-questions.md) | GET | Retrieves campaign questions from Sage Sales Management. |
| [List Campaign Statuses](actions/list-campaign-statuses.md) | GET | Retrieves campaign statuses from Sage Sales Management. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Sage Sales Management. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from Sage Sales Management. |
| [List Opportunity Statuses](actions/list-opportunity-statuses.md) | GET | Retrieves opportunity statuses from Sage Sales Management. |
| [List Opportunity Types](actions/list-opportunity-types.md) | GET | Retrieves opportunity types from Sage Sales Management. |
| [List Sales](actions/list-sales.md) | GET | Retrieves sales from Sage Sales Management. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an opportunity in Sage Sales Management. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Sage Sales Management. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from Sage Sales Management. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Sage Sales Management. |
| [Get Product Categories Schema](actions/get-product-categories-schema.md) | GET | Retrieves the product categories schema from Sage Sales Management. |
| [Get Product Families Schema](actions/get-product-families-schema.md) | GET | Retrieves the product families schema from Sage Sales Management. |
| [Get Product Rate](actions/get-product-rate.md) | GET | Retrieves a product rate from Sage Sales Management. |
| [Get Product Rates Schema](actions/get-product-rates-schema.md) | GET | Retrieves the product rates schema from Sage Sales Management. |
| [Get Products Schema](actions/get-products-schema.md) | GET | Retrieves the products schema from Sage Sales Management. |
| [Get Rate](actions/get-rate.md) | GET | Retrieves a rate from Sage Sales Management. |
| [Get Rates Schema](actions/get-rates-schema.md) | GET | Retrieves the rates schema from Sage Sales Management. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product categories from Sage Sales Management. |
| [List Product Families](actions/list-product-families.md) | GET | Retrieves product families from Sage Sales Management. |
| [List Product Rates](actions/list-product-rates.md) | GET | Retrieves product rates from Sage Sales Management. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Sage Sales Management. |
| [List Rates](actions/list-rates.md) | GET | Retrieves rates from Sage Sales Management. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Sage Sales Management. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a sales order in Sage Sales Management. |
| [Delete Sales Order](actions/delete-sales-order.md) | DELETE | Deletes a sales order from Sage Sales Management. |
| [Get Order Line](actions/get-order-line.md) | GET | Retrieves an order line from Sage Sales Management. |
| [Get Order Lines Schema](actions/get-order-lines-schema.md) | GET | Retrieves the order lines schema from Sage Sales Management. |
| [Get Order Status](actions/get-order-status.md) | GET | Retrieves an order status from Sage Sales Management. |
| [Get Order Statuses Schema](actions/get-order-statuses-schema.md) | GET | Retrieves the order statuses schema from Sage Sales Management. |
| [Get Order Type](actions/get-order-type.md) | GET | Retrieves an order type from Sage Sales Management. |
| [Get Order Types Schema](actions/get-order-types-schema.md) | GET | Retrieves the order types schema from Sage Sales Management. |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Sage Sales Management. |
| [Get Sales Orders Schema](actions/get-sales-orders-schema.md) | GET | Retrieves the sales orders schema from Sage Sales Management. |
| [List Order Lines](actions/list-order-lines.md) | GET | Retrieves order lines from Sage Sales Management. |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves order statuses from Sage Sales Management. |
| [List Order Types](actions/list-order-types.md) | GET | Retrieves order types from Sage Sales Management. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Sage Sales Management. |
| [Update Sales Order](actions/update-sales-order.md) | PUT | Updates a sales order in Sage Sales Management. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates an activity in Sage Sales Management. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an activity from Sage Sales Management. |
| [Get Activities Schema](actions/get-activities-schema.md) | GET | Retrieves the activities schema from Sage Sales Management. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Sage Sales Management. |
| [Get Activity Type](actions/get-activity-type.md) | GET | Retrieves an activity type from Sage Sales Management. |
| [Get Activity Types Schema](actions/get-activity-types-schema.md) | GET | Retrieves the activity types schema from Sage Sales Management. |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar entry from Sage Sales Management. |
| [Get Calendar Schema](actions/get-calendar-schema.md) | GET | Retrieves the calendar schema from Sage Sales Management. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Sage Sales Management. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Sage Sales Management. |
| [List Activity Points](actions/list-activity-points.md) | GET | Retrieves activity points from Sage Sales Management. |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from Sage Sales Management. |
| [List Calendar](actions/list-calendar.md) | GET | Retrieves calendar entries from Sage Sales Management. |
| [List Document Folders](actions/list-document-folders.md) | GET | Retrieves document folders from Sage Sales Management. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Sage Sales Management. |
| [List News](actions/list-news.md) | GET | Retrieves news from Sage Sales Management. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Sage Sales Management. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an activity in Sage Sales Management. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Owners Schema](actions/get-entity-owners-schema.md) | GET | Retrieves the entity owners schema from Sage Sales Management. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Sage Sales Management. |
| [Get Roles Schema](actions/get-roles-schema.md) | GET | Retrieves the roles schema from Sage Sales Management. |
| [Get User](actions/get-user.md) | GET | Retrieves an user from Sage Sales Management. |
| [Get User Type](actions/get-user-type.md) | GET | Retrieves an user type from Sage Sales Management. |
| [Get User Types Schema](actions/get-user-types-schema.md) | GET | Retrieves the user types schema from Sage Sales Management. |
| [Get Users Schema](actions/get-users-schema.md) | GET | Retrieves the users schema from Sage Sales Management. |
| [List Entity Owners](actions/list-entity-owners.md) | GET | Retrieves entity owners from Sage Sales Management. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Sage Sales Management. |
| [List Roles of User](actions/list-roles-of-user.md) | GET | Retrieves roles for a user from Sage Sales Management. |
| [List User Hierarchy](actions/list-user-hierarchy.md) | GET | Retrieves the user hierarchy from Sage Sales Management. |
| [List User Scores](actions/list-user-scores.md) | GET | Retrieves user scores from Sage Sales Management. |
| [List User Types](actions/list-user-types.md) | GET | Retrieves user types from Sage Sales Management. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Sage Sales Management. |
| [List Users in Role](actions/list-users-in-role.md) | GET | Retrieves users in a role from Sage Sales Management. |
| [Login](actions/login.md) | GET | Retrieves a session key from Sage Sales Management. |

