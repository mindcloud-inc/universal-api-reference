# HubSpot: Native API Reference

A consolidated summary of HubSpot's API configuration and 75 documented operations, with links to official documentation.

- **Official docs:** https://developers.hubspot.com/docs/api-reference/latest/overview
- **REST - Query Pagination base URL:** `https://api.hubapi.com`
- **REST - Body Pagination base URL:** `https://api.hubapi.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.hubspot.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.hubapi.com/oauth/v1/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `crm.schemas.companies.write crm.schemas.quotes.read crm.objects.line_items.read crm.schemas.deals.read crm.objects.line_items.write crm.schemas.deals.write crm.schemas.line_items.read crm.schemas.orders.read crm.objects.orders.write oauth crm.objects.owners.read crm.objects.orders.read crm.objects.invoices.read crm.schemas.invoices.read account-info.security.read crm.objects.products.read tickets crm.objects.contacts.write crm.objects.products.write crm.schemas.custom.read crm.objects.invoices.write crm.objects.custom.read crm.objects.custom.write crm.objects.companies.write crm.lists.write crm.objects.companies.read crm.schemas.listings.read crm.lists.read settings.users.read crm.objects.deals.read crm.schemas.contacts.read crm.objects.deals.write crm.objects.quotes.write crm.objects.contacts.read crm.schemas.companies.read crm.objects.quotes.read`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.hubapi.com/oauth/v1/token.

[Official authentication documentation](https://developers.hubspot.com/docs/api-reference/auth-oauth-v1/guide)

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

### REST - Query Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `paging.next.after`.

### REST - Body Pagination

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `paging.next.after`.

## Pagination

- **REST - Query Pagination:** Use `limit` in the query string to set the page size (default 100; accepted range 10–100). Use `after` in the query string as the pagination cursor.
- **REST - Body Pagination:** Use `limit` in the request body to set the page size (default 200; accepted range 10–200). Use `after` in the request body as the pagination cursor.

## Filtering

- **REST - Body Pagination:** Send filters in the request body. Supported operators: `between`, `contain`, `eq`, `exist`, `gt`, `gte`, `lt`, `lte`, `ncontain`, `ne`, `nexist`.

## Endpoints (75 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Add User](actions/add-user.md) | REST - Query Pagination | `POST settings/v3/users/` | [docs](https://developers.hubspot.com/docs/api-reference/settings-user-provisioning-v3/users/post-settings-v3-users-) |
| [Batch Create Orders](actions/batch-create-orders.md) | REST - Query Pagination | `POST crm/v3/objects/orders/batch/create` | [docs](https://developers.hubspot.com/docs/api-reference/crm-orders-v3/batch/post-crm-v3-objects-orders-batch-create) |
| [Batch Read Contacts](actions/batch-read-contacts.md) | REST - Query Pagination | `POST crm/v3/objects/contacts/batch/read` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/batch/post-crm-v3-objects-contacts-batch-read) |
| [Batch Read Engagements](actions/batch-read-engagements.md) | REST - Query Pagination | `POST crm/v3/objects/:engagementType/batch/read` | [docs](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/batch/post-crm-v3-objects-objectType-batch-read) |
| [Batch Read Line Items](actions/batch-read-line-items.md) | REST - Query Pagination | `POST crm/v3/objects/line_items/batch/read` | [docs](https://developers.hubspot.com/docs/api-reference/crm-line-items-v3/batch/post-crm-v3-objects-line_items-batch-read) |
| [Batch Read Notes](actions/batch-read-notes.md) | REST - Query Pagination | `POST crm/v3/objects/notes/batch/read` | [docs](https://developers.hubspot.com/docs/api-reference/crm-notes-v3/batch/post-crm-v3-objects-notes-batch-read) |
| [Create Company](actions/create-company.md) | REST - Query Pagination | `POST crm/v3/objects/companies` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/post-crm-v3-objects-companies) |
| [Create Contact](actions/create-contact.md) | REST - Query Pagination | `POST crm/v3/objects/contacts` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/post-crm-v3-objects-contacts) |
| [Create Deal](actions/create-deal.md) | REST - Query Pagination | `POST crm/v3/objects/deals` | [docs](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/post-crm-v3-objects-0-3) |
| [Create Engagement](actions/create-engagement.md) | REST - Query Pagination | `POST crm/v3/objects/:engagementType` | [docs](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/basic/post-crm-v3-objects-objectType) |
| [Create Line Item](actions/create-line-item.md) | REST - Query Pagination | `POST crm/v3/objects/line_items` | [docs](https://developers.hubspot.com/docs/api-reference/crm-line-items-v3/guide) |
| [Create List](actions/create-list.md) | REST - Query Pagination | `POST crm/v3/lists` | [docs](https://developers.hubspot.com/docs/api-reference/crm-lists-v3/lists/post-crm-v3-lists) |
| [Create Object Schema](actions/create-object-schema.md) | REST - Query Pagination | `POST crm-object-schemas/v3/schemas` | [docs](https://developers.hubspot.com/docs/api-reference/crm-schemas-v3/core/post-crm-object-schemas-v3-schemas) |
| [Create Pipeline Stage](actions/create-pipeline-stage.md) | REST - Query Pagination | `POST crm/v3/pipelines/:objectType/:pipelineId/stages` | [docs](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipeline-stages/post-crm-v3-pipelines-objectType-pipelineId-stages) |
| [Create Product](actions/create-product.md) | REST - Query Pagination | `POST crm/v3/objects/products` | [docs](https://developers.hubspot.com/docs/api-reference/crm-products-v3/basic/post-crm-v3-objects-products) |
| [Create Property](actions/create-property.md) | REST - Query Pagination | `POST crm/v3/properties/:objectType` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/post-crm-v3-properties-objectType) |
| [Create Quote](actions/create-quote.md) | REST - Query Pagination | `POST crm/v3/objects/quotes` | [docs](https://developers.hubspot.com/docs/api-reference/crm-quotes-v3/basic/post-crm-v3-objects-quotes) |
| [Delete Association](actions/delete-association.md) | REST - Query Pagination | `DELETE crm/v4/objects/:objectType/:objectId/associations/:toObjectType/:toObjectId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-associations-v4/basic/delete-crm-v4-objects-objectType-objectId-associations-toObjectType-toObjectId) |
| [Delete Company by ID](actions/delete-company-by-id.md) | REST - Query Pagination | `DELETE crm/v3/objects/companies/:companyId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/delete-crm-v3-objects-companies-companyId) |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | REST - Query Pagination | `DELETE crm/v3/objects/contacts/:contactId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/delete-crm-v3-objects-contacts-contactId) |
| [Delete Property](actions/delete-property.md) | REST - Query Pagination | `DELETE crm/v3/properties/:objectType/:propertyName` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/delete-crm-v3-properties-objectType-propertyName) |
| [Delete Ticket by ID](actions/delete-ticket-by-id.md) | REST - Query Pagination | `DELETE crm/v3/objects/tickets/:ticketId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/basic/delete-crm-v3-objects-tickets-ticketId) |
| [Get Account Info](actions/get-account-info.md) | REST - Query Pagination | `GET account-info/v3/details` | [docs](https://developers.hubspot.com/docs/api-reference/account-account-info-v3/details/get-account-info-v3-details) |
| [Get Company by ID](actions/get-company-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/companies/:companyId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/get-crm-v3-objects-companies-companyId) |
| [Get Company Industries](actions/get-company-industries.md) | REST - Query Pagination | `GET crm/v3/properties/companies/industry` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType-propertyName) |
| [Get Contact by ID](actions/get-contact-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/contacts/:contactId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts-contactId) |
| [Get Deal by ID](actions/get-deal-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/deals/:dealId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/get-crm-v3-objects-0-3-dealId) |
| [Get Email](actions/get-email.md) | REST - Query Pagination | `GET crm/v3/objects/emails/:emailId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-emails-v3/basic/get-crm-v3-objects-emails-emailId) |
| [Get File Details](actions/get-file-details.md) | REST - Query Pagination | `GET files/v3/files/:fileId` | [docs](https://developers.hubspot.com/docs/api-reference/files-files-v3/files/get-files-v3-files-fileId) |
| [Get Listing By ID](actions/get-listing-by-id.md) | REST - Query Pagination | `GET crm/objects/2026-03/:objectTypeId/:objectId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts-contactId) |
| [Get Owner](actions/get-owner.md) | REST - Query Pagination | `GET crm/v3/owners/:ownerId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-crm-owners-v3/owners/get-crm-v3-owners-ownerId) |
| [Get Pipeline by ID](actions/get-pipeline-by-id.md) | REST - Query Pagination | `GET crm/v3/pipelines/:objectType/:pipelineId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipelines/get-crm-v3-pipelines-objectType-pipelineId) |
| [Get Pipeline Stage by ID](actions/get-pipeline-stage-by-id.md) | REST - Query Pagination | `GET crm/v3/pipelines/:objectType/:pipelineId/stages/:stageId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipeline-stages/get-crm-v3-pipelines-objectType-pipelineId-stages-stageId) |
| [Get Property Details](actions/get-property-details.md) | REST - Query Pagination | `GET crm/v3/properties/:objectType/:propertyName` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType-propertyName) |
| [Get Quote by ID](actions/get-quote-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/quotes/:quoteId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-quotes-v3/basic/get-crm-v3-objects-quotes-quoteId) |
| [Get Shipping Method](actions/get-shipping-method.md) | REST - Query Pagination | `GET crm/v3/properties/deals/shipping_method` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType-propertyName) |
| [Get Subscription by ID](actions/get-subscription-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/subscriptions/:subscriptionId` | [docs](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/commerce-subscriptions/get-commerce-subscription) |
| [Get Ticket by ID](actions/get-ticket-by-id.md) | REST - Query Pagination | `GET crm/v3/objects/tickets/:ticketId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/basic/get-crm-v3-objects-tickets-ticketId) |
| [Get User](actions/get-user.md) | REST - Query Pagination | `GET crm/v3/objects/users/:userId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-users-v3/basic/get-crm-v3-objects-users-userId) |
| [List Associations](actions/list-associations.md) | REST - Query Pagination | `GET crm/v4/objects/:fromObject/:objectId/associations/:toObjectType` | [docs](https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide) |
| [List Business Units for User](actions/list-business-units-for-user.md) | REST - Query Pagination | `GET business-units/v3/business-units/user/:userId` | [docs](https://developers.hubspot.com/docs/api-reference/business-units-business-units-v3/business-unit/get-business-units-v3-business-units-user-userId) |
| [List Companies](actions/list-companies.md) | REST - Query Pagination | `GET crm/v3/objects/companies` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/get-crm-v3-objects-companies) |
| [List Company Contacts](actions/list-company-contacts.md) | REST - Query Pagination | `GET crm/v3/objects/companies/:companyId/associations/contacts` | [docs](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations) |
| [List Company Contacts v2026-03](actions/list-company-contacts-v202603.md) | REST - Query Pagination | `GET crm/2026-03/objects/companies/:companyId/associations/contacts` | [docs](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations) |
| [List Contact Companies](actions/list-contact-companies.md) | REST - Query Pagination | `GET crm/v3/objects/contacts/:contactId/associations/companies` | [docs](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations) |
| [List Contacts](actions/list-contacts.md) | REST - Query Pagination | `GET crm/v3/objects/contacts` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts) |
| [List Deal Line Items](actions/list-deal-line-items.md) | REST - Query Pagination | `GET crm/v3/objects/deals/:dealId/associations/line_items` | [docs](https://developers.hubspot.com/docs/api-reference/crm-associations-v3/guide) |
| [List Deal Quotes](actions/list-deal-quotes.md) | REST - Query Pagination | `GET crm/v3/objects/deals/:dealId/associations/quotes` | [docs](https://developers.hubspot.com/docs/api-reference/crm-associations-v3/guide) |
| [List Deals](actions/list-deals.md) | REST - Query Pagination | `GET crm/v3/objects/deals` | [docs](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/get-crm-v3-objects-0-3) |
| [List Emails](actions/list-emails.md) | REST - Query Pagination | `GET crm/v3/objects/emails` | [docs](https://developers.hubspot.com/docs/api-reference/crm-emails-v3/basic/get-crm-v3-objects-emails) |
| [List Forms](actions/list-forms.md) | REST - Query Pagination | `GET forms/v2/forms` | [docs](https://developers.hubspot.com/docs/api-reference/legacy/forms-v2/forms/get-forms-v2-forms) |
| [List Owners](actions/list-owners.md) | REST - Query Pagination | `GET crm/v3/owners/` | [docs](https://developers.hubspot.com/docs/api-reference/crm-crm-owners-v3/owners/get-crm-v3-owners-) |
| [List Pipelines](actions/list-pipelines.md) | REST - Query Pagination | `GET crm/v3/pipelines/:objectType` | [docs](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipelines/get-crm-v3-pipelines-objectType) |
| [List Properties](actions/list-properties.md) | REST - Query Pagination | `GET crm/v3/properties/:objectType` | [docs](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/get-crm-v3-properties-objectType) |
| [List Subscriptions](actions/list-subscriptions.md) | REST - Query Pagination | `GET crm/v3/objects/subscriptions` | [docs](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/commerce-subscriptions/get-commerce-subscriptions) |
| [List Tickets](actions/list-tickets.md) | REST - Query Pagination | `GET crm/v3/objects/tickets` | [docs](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/basic/get-crm-v3-objects-tickets) |
| [List Users](actions/list-users.md) | REST - Query Pagination | `GET settings/v3/users` | [docs](https://developers.hubspot.com/docs/api-reference/settings-user-provisioning-v3/users/get-settings-v3-users-) |
| [Search Companies](actions/search-companies.md) | REST - Body Pagination | `POST crm/v3/objects/companies/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/search/post-crm-v3-objects-companies-search) |
| [Search Contacts](actions/search-contacts.md) | REST - Body Pagination | `POST crm/v3/objects/contacts/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/search/post-crm-v3-objects-contacts-search) |
| [Search Deals](actions/search-deals.md) | REST - Body Pagination | `POST crm/v3/objects/deals/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/search/post-crm-v3-objects-0-3-search) |
| [Search Engagements](actions/search-engagements.md) | REST - Body Pagination | `POST crm/v3/objects/:engagementType/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/search/post-crm-v3-objects-objectType-search) |
| [Search Files](actions/search-files.md) | REST - Query Pagination | `GET files/v3/files/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts) |
| [Search Invoices](actions/search-invoices.md) | REST - Body Pagination | `POST crm/v3/objects/invoices/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-invoices-v3/search/post-crm-v3-objects-invoices-search) |
| [Search Lists](actions/search-lists.md) | REST - Body Pagination | `POST crm/v3/lists/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-lists-v3/lists/post-crm-v3-lists-search) |
| [Search Orders](actions/search-orders.md) | REST - Body Pagination | `POST crm/v3/objects/orders/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-orders-v3/search/post-crm-v3-objects-orders-search) |
| [Search Products](actions/search-products.md) | REST - Body Pagination | `POST crm/v3/objects/products/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-products-v3/search/post-crm-v3-objects-products-search) |
| [Search Subscriptions](actions/search-subscriptions.md) | REST - Body Pagination | `POST crm/v3/objects/subscriptions/search` | [docs](https://developers.hubspot.com/docs/api-reference/legacy/crm/objects/commerce-subscriptions/search/search-commerce-subscriptions) |
| [Search Tickets](actions/search-tickets.md) | REST - Body Pagination | `POST crm/v3/objects/tickets/search` | [docs](https://developers.hubspot.com/docs/api-reference/crm-tickets-v3/search/post-crm-v3-objects-tickets-search) |
| [Update Company by ID](actions/update-company-by-id.md) | REST - Query Pagination | `PATCH crm/v3/objects/companies/:companyId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/patch-crm-v3-objects-companies-companyId) |
| [Update Contact by ID](actions/update-contact-by-id.md) | REST - Query Pagination | `PATCH crm/v3/objects/contacts/:contactId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/patch-crm-v3-objects-contacts-contactId) |
| [Update Custom Object Record](actions/update-custom-object-record.md) | REST - Query Pagination | `PATCH crm/v3/objects/:objectType/:objectId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-custom-objects-v3/guide) |
| [Update Deal by ID](actions/update-deal-by-id.md) | REST - Query Pagination | `PATCH crm/v3/objects/deals/:dealId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-deals-v3/basic/patch-crm-v3-objects-deals-dealId) |
| [Update Engagement by ID](actions/update-engagement-by-id.md) | REST - Query Pagination | `PATCH crm/v3/objects/:engagementType/:engagementId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/basic/patch-crm-v3-objects-objectType-objectId) |
| [Update Invoice by ID](actions/update-invoice-by-id.md) | REST - Query Pagination | `PATCH crm/v3/objects/invoices/:invoiceId` | [docs](https://developers.hubspot.com/docs/api-reference/crm-invoices-v3/basic/patch-crm-v3-objects-invoices-invoiceId) |
| [Upload Files](actions/upload-files.md) | REST - Query Pagination | `POST files/v3/files` | [docs](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts) |
