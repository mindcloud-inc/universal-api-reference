# Sage Sales Management: Native API Reference

A consolidated summary of Sage Sales Management's API configuration and 129 documented operations, with links to official documentation.

- **Official docs:** https://developer.forcemanager.com/
- **API base URL:** `https://api.forcemanager.com/api/v4`

## Authentication

### Session Login

Uses the Sage Sales Management v4 login endpoint with the tenant public and private API keys, then sends the returned session token as X-Session-Key on subsequent requests.

### Credentials

- **Public API Key:** `publicKey` · required · The Sage Sales Management public API key used as the login username.
- **Private API Key:** `privateKey` · required · The Sage Sales Management private API key used as the login password.

Send these headers with each API request:

```http
X-Session-Key: <custom.token>
```

[Official authentication documentation](https://support.forcemanager.net/en/articles/8613476-authentication-in-sage-sales-management-api)

## Endpoints (129 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://developer.forcemanager.com/) |
| [Create Activity](actions/create-activity.md) | `POST /activities` | [docs](https://developer.forcemanager.com/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.forcemanager.com/) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /opportunities` | [docs](https://developer.forcemanager.com/) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://developer.forcemanager.com/) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /salesorders` | [docs](https://developer.forcemanager.com/) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /activities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /opportunities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Delete Sales Order](actions/delete-sales-order.md) | `DELETE /salesorders/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Account](actions/get-account.md) | `GET /accounts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Account Address](actions/get-account-address.md) | `GET /accountAddresses/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Account Addresses Schema](actions/get-account-addresses-schema.md) | `GET /accountAddresses/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Account Segments Schema](actions/get-account-segments-schema.md) | `GET /accountSegments/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Account Statuses Schema](actions/get-account-statuses-schema.md) | `GET /accountStatuses/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Account Types Schema](actions/get-account-types-schema.md) | `GET /accountTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Accounts Schema](actions/get-accounts-schema.md) | `GET /accounts/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Activities Schema](actions/get-activities-schema.md) | `GET /activities/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Activity](actions/get-activity.md) | `GET /activities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Activity Type](actions/get-activity-type.md) | `GET /activityTypes/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Activity Types Schema](actions/get-activity-types-schema.md) | `GET /activityTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Branch](actions/get-branch.md) | `GET /branches/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Branches Schema](actions/get-branches-schema.md) | `GET /branches/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Calendar](actions/get-calendar.md) | `GET /calendar/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Calendar Schema](actions/get-calendar-schema.md) | `GET /calendar/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Call](actions/get-call.md) | `GET /calls/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Campaign Question](actions/get-campaign-question.md) | `GET /campaignQuestions/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Contact Types Schema](actions/get-contact-types-schema.md) | `GET /contactTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Contacts Schema](actions/get-contacts-schema.md) | `GET /contacts/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Countries Schema](actions/get-countries-schema.md) | `GET /countries/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Currencies Schema](actions/get-currencies-schema.md) | `GET /currencies/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Email](actions/get-email.md) | `GET /emails/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Emails Schema](actions/get-emails-schema.md) | `GET /emails/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Entity Contacts Schema](actions/get-entity-contacts-schema.md) | `GET /contactsEntities/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Entity Owners Schema](actions/get-entity-owners-schema.md) | `GET /entityOwners/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Opportunities Schema](actions/get-opportunities-schema.md) | `GET /opportunities/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /opportunities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Opportunity Statuses Schema](actions/get-opportunity-statuses-schema.md) | `GET /opportunityStatuses/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Opportunity Types Schema](actions/get-opportunity-types-schema.md) | `GET /opportunityTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Order Line](actions/get-order-line.md) | `GET /salesordersLines/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Order Lines Schema](actions/get-order-lines-schema.md) | `GET /salesordersLines/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Order Status](actions/get-order-status.md) | `GET /salesorderStatuses/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Order Statuses Schema](actions/get-order-statuses-schema.md) | `GET /salesorderStatuses/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Order Type](actions/get-order-type.md) | `GET /orderTypes/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Order Types Schema](actions/get-order-types-schema.md) | `GET /orderTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Product](actions/get-product.md) | `GET /products/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Product Categories Schema](actions/get-product-categories-schema.md) | `GET /productCategories/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Product Families Schema](actions/get-product-families-schema.md) | `GET /productFamilies/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Product Rate](actions/get-product-rate.md) | `GET /productRates/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Product Rates Schema](actions/get-product-rates-schema.md) | `GET /productRates/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Products Schema](actions/get-products-schema.md) | `GET /products/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Rate](actions/get-rate.md) | `GET /rates/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Rates Schema](actions/get-rates-schema.md) | `GET /rates/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Related Account](actions/get-related-account.md) | `GET /accountsRelated/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Related Account Type](actions/get-related-account-type.md) | `GET /accountsRelations/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Related Account Types Schema](actions/get-related-account-types-schema.md) | `GET /accountsRelations/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Related Accounts Schema](actions/get-related-accounts-schema.md) | `GET /accountsRelated/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Resources](actions/get-resources.md) | `GET /resources` | [docs](https://developer.forcemanager.com/) |
| [Get Resources by Phone Number](actions/get-resources-by-phone-number.md) | `GET /calls/phone/{{phoneNumber}}` | [docs](https://developer.forcemanager.com/) |
| [Get Role](actions/get-role.md) | `GET /roles/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Roles Schema](actions/get-roles-schema.md) | `GET /roles/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Sale](actions/get-sale.md) | `GET /sales/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /salesorders/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get Sales Orders Schema](actions/get-sales-orders-schema.md) | `GET /salesorders/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Sales Schema](actions/get-sales-schema.md) | `GET /sales/schema` | [docs](https://developer.forcemanager.com/) |
| [Get User](actions/get-user.md) | `GET /users/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get User Type](actions/get-user-type.md) | `GET /userTypes/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Get User Types Schema](actions/get-user-types-schema.md) | `GET /userTypes/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Users Schema](actions/get-users-schema.md) | `GET /users/schema` | [docs](https://developer.forcemanager.com/) |
| [Get Webhook](actions/get-webhook.md) | `GET /hooks/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [List Account Addresses](actions/list-account-addresses.md) | `GET /accountAddresses` | [docs](https://developer.forcemanager.com/) |
| [List Account Segments](actions/list-account-segments.md) | `GET /accountSegments` | [docs](https://developer.forcemanager.com/) |
| [List Account Statuses](actions/list-account-statuses.md) | `GET /accountStatuses` | [docs](https://developer.forcemanager.com/) |
| [List Account Types](actions/list-account-types.md) | `GET /accountTypes` | [docs](https://developer.forcemanager.com/) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developer.forcemanager.com/) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://developer.forcemanager.com/) |
| [List Activity Points](actions/list-activity-points.md) | `GET /activity/points` | [docs](https://developer.forcemanager.com/) |
| [List Activity Types](actions/list-activity-types.md) | `GET /activityTypes` | [docs](https://developer.forcemanager.com/) |
| [List Branches](actions/list-branches.md) | `GET /branches` | [docs](https://developer.forcemanager.com/) |
| [List Calendar](actions/list-calendar.md) | `GET /calendar` | [docs](https://developer.forcemanager.com/) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://developer.forcemanager.com/) |
| [List Campaign Questions](actions/list-campaign-questions.md) | `GET /campaignQuestions` | [docs](https://developer.forcemanager.com/) |
| [List Campaign Statuses](actions/list-campaign-statuses.md) | `GET /campaignStatuses` | [docs](https://developer.forcemanager.com/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developer.forcemanager.com/) |
| [List Contact Types](actions/list-contact-types.md) | `GET /contactTypes` | [docs](https://developer.forcemanager.com/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.forcemanager.com/) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://developer.forcemanager.com/) |
| [List Currencies](actions/list-currencies.md) | `GET /currencies` | [docs](https://developer.forcemanager.com/) |
| [List Document Folders](actions/list-document-folders.md) | `GET /documents/folders` | [docs](https://developer.forcemanager.com/) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developer.forcemanager.com/) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://developer.forcemanager.com/) |
| [List Entity Contacts](actions/list-entity-contacts.md) | `GET /contactsEntities` | [docs](https://developer.forcemanager.com/) |
| [List Entity Owners](actions/list-entity-owners.md) | `GET /entityOwners` | [docs](https://developer.forcemanager.com/) |
| [List News](actions/list-news.md) | `GET /news` | [docs](https://developer.forcemanager.com/) |
| [List Opportunities](actions/list-opportunities.md) | `GET /opportunities` | [docs](https://developer.forcemanager.com/) |
| [List Opportunity Statuses](actions/list-opportunity-statuses.md) | `GET /opportunityStatuses` | [docs](https://developer.forcemanager.com/) |
| [List Opportunity Types](actions/list-opportunity-types.md) | `GET /opportunityTypes` | [docs](https://developer.forcemanager.com/) |
| [List Order Lines](actions/list-order-lines.md) | `GET /salesordersLines` | [docs](https://developer.forcemanager.com/) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /salesorderStatuses` | [docs](https://developer.forcemanager.com/) |
| [List Order Types](actions/list-order-types.md) | `GET /orderTypes` | [docs](https://developer.forcemanager.com/) |
| [List Product Categories](actions/list-product-categories.md) | `GET /productCategories` | [docs](https://developer.forcemanager.com/) |
| [List Product Families](actions/list-product-families.md) | `GET /productFamilies` | [docs](https://developer.forcemanager.com/) |
| [List Product Rates](actions/list-product-rates.md) | `GET /productRates` | [docs](https://developer.forcemanager.com/) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://developer.forcemanager.com/) |
| [List Rates](actions/list-rates.md) | `GET /rates` | [docs](https://developer.forcemanager.com/) |
| [List Related Account Types](actions/list-related-account-types.md) | `GET /accountsRelations` | [docs](https://developer.forcemanager.com/) |
| [List Related Accounts](actions/list-related-accounts.md) | `GET /accountsRelated` | [docs](https://developer.forcemanager.com/) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://developer.forcemanager.com/) |
| [List Roles of User](actions/list-roles-of-user.md) | `GET /users/{{id}}/roles` | [docs](https://developer.forcemanager.com/) |
| [List Sales](actions/list-sales.md) | `GET /sales` | [docs](https://developer.forcemanager.com/) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /salesorders` | [docs](https://developer.forcemanager.com/) |
| [List Time Zones](actions/list-time-zones.md) | `GET /timezones` | [docs](https://developer.forcemanager.com/) |
| [List User Hierarchy](actions/list-user-hierarchy.md) | `GET /users/{{id}}/hierarchy` | [docs](https://developer.forcemanager.com/) |
| [List User Scores](actions/list-user-scores.md) | `GET /users/scores` | [docs](https://developer.forcemanager.com/) |
| [List User Types](actions/list-user-types.md) | `GET /userTypes` | [docs](https://developer.forcemanager.com/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.forcemanager.com/) |
| [List Users in Role](actions/list-users-in-role.md) | `GET /roles/{{id}}/users` | [docs](https://developer.forcemanager.com/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /hooks` | [docs](https://developer.forcemanager.com/) |
| [Login](actions/login.md) | `POST /login` | [docs](https://developer.forcemanager.com/) |
| [Update Account](actions/update-account.md) | `PUT /accounts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Update Activity](actions/update-activity.md) | `PUT /activities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT /opportunities/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Update Product](actions/update-product.md) | `PUT /products/{{id}}` | [docs](https://developer.forcemanager.com/) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /salesorders/{{id}}` | [docs](https://developer.forcemanager.com/) |
