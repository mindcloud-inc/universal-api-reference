# Salesforce: Native API Reference

A consolidated summary of Salesforce's API configuration and 30 documented operations.

- **REST base URL:** `https://{companyDomainName}.my.salesforce.com`
- **REST SOQL Read base URL:** `https://{companyDomainName}.my.salesforce.com`
- **REST Deleted Records Read base URL:** `https://{companyDomainName}.my.salesforce.com`

## Authentication

### OAuth 2.0

### Credentials

- **Company Domain Name:** `companyDomainName` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.companyDomainName}}.my.salesforce.com/services/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.companyDomainName}}.my.salesforce.com/services/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `full refresh_token api offline_access`.

Refresh expired access tokens with a POST request to https://{{credentials.companyDomainName}}.my.salesforce.com/services/oauth2/token.

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientName` | path | `string` | yes | Name of the client for the API subdomain |

### REST SOQL Read

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `records`. The next-page cursor is read from `nextRecordsUrl`.

### REST Deleted Records Read

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST:** Use `limit` in the request parameters to set the page size (default 25; accepted range 1–200). Use `offset` in the request parameters as the record offset.
- **REST SOQL Read:** Use `cursor` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Sorting

- **REST SOQL Read:** Set the sort field with `orderBy` in the query string. Set the direction separately with `direction`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

- **REST:** Stop after 50 attempts. Multiply the delay by 3 after each failed attempt.
- **REST SOQL Read:** Retry responses with status codes `503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
- **REST Deleted Records Read:** Retry responses with status codes `503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Create Account](actions/create-account.md) | REST | `POST services/data/v62.0/sobjects/Account` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_account.htm) |
| [Create Customer](actions/create-customer.md) | REST | `POST services/data/v62.0/sobjects/Contact` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_contact.htm) |
| [Create Order](actions/create-order.md) | REST | `POST /services/data/v64.0/sobjects/Order` |  |
| [Create Order Item](actions/create-order-item.md) | REST | `POST /services/data/v64.0/sobjects/OrderItem` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_orderitem.htm) |
| [Create Product](actions/create-product.md) | REST | `POST /services/data/v64.0/sobjects/Product2` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_product2.htm) |
| [Create Record](actions/create-record.md) | REST | `POST services/data/v61.0/sobjects/:objectId/` |  |
| [Delete Record](actions/delete-record.md) | REST | `DELETE services/data/v61.0/sobjects/:objectId/:recordId` |  |
| [Find Product Offer by Product Code](actions/find-product-by-product-code.md) | REST | `GET services/data/v61.0/query?q=SELECT+Id,+ProductCode,+UPC__c,+%28SELECT+Quantity__c,+Consumed_Quantity__c,+id,+Vendor_ID__c,+Vendor_Offer__c+FROM Offers__r%29+FROM+Product2+WHERE+ProductCode+=+':productcode'` |  |
| [Get Contact by Email](actions/get-contact-by-email.md) | REST | `GET services/data/v61.0/query` |  |
| [Get Contacts](actions/get-contacts.md) | REST | `GET services/data/v61.0/query?q=SELECT+Id,+FirstName,+LastName,+Title,+Email,+MobilePhone,+Department+FROM+Contact` |  |
| [Get Deleted Quote Line Items](actions/get-deleted-quote-line-items.md) | REST Deleted Records Read | `GET /services/data/v61.0/sobjects/QuoteLineItem/deleted/` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-getdeleted.html) |
| [Get Fulfillment Orders](actions/get-fulfillment-orders.md) | REST | `GET services/data/v61.0/query` |  |
| [Find Order by OrderNumber](actions/get-order.md) | REST | `GET services/data/v61.0/query?q=SELECT+Id+FROM+Order+WHERE+Customer_PO__c=':orderNumber'` |  |
| [Get Order Delivery Group](actions/get-order-delivery-group.md) | REST | `GET services/data/v61.0/query` |  |
| [Get Order Delivery Method](actions/get-order-delivery-method.md) | REST | `GET services/data/v61.0/query` |  |
| [List Billing Credit Notes](actions/list-billing-credit-notes.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Billing Invoices](actions/list-billing-invoices.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Credit Memos](actions/list-credit-memos.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Invoices](actions/list-invoices.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Orders](actions/list-orders.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Pricebook](actions/list-pricebook.md) | REST | `GET /services/data/v56.0/query?q=SELECT+Id,+Name,+IsActive,+IsArchived,+IsDeleted,+IsStandard,+LastReferencedDate,+ValidFrom,+ValidTo,+LastViewedDate,+Description+FROM+Pricebook2` |  |
| [List Pricebook Entry](actions/list-pricebook-entry.md) | REST | `GET /services/data/v56.0/query?q=SELECT+Id,+Product2Id,+Pricebook2Id,+Name,+ActivePriceAdjustmentQuantity,+IsActive,+IsArchived,+ProductCode,+ProductSellingModelId,+UseStandardPrice,+UnitPrice+FROM+PricebookEntry` |  |
| [List Quote Line Items](actions/list-quote-line-items.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [List Quotes](actions/list-quotes.md) | REST SOQL Read | `GET /services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query) |
| [Org sObjects (Lookup)](actions/lookup-s-objects.md) | REST | `GET services/data/v61.0/sobjects/` | [docs](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_describe.htm) |
| [Query (SOQL)](actions/query.md) | REST | `GET services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_select.htm) |
| [Query Order Items (test)](actions/query-order-items-test.md) | REST | `GET services/data/v61.0/query` |  |
| [Update Order Items](actions/update-invoice.md) | REST | `PATCH services/data/v61.0/sobjects/OrderItem/:id` |  |
| [Update Product](actions/update-product.md) | REST | `PATCH /services/data/v64.0/sobjects/Product2/:id` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_product2.htm) |
| [Update Record](actions/update-recordv2.md) | REST | `PATCH services/data/v61.0/sobjects/:objectId/:recordId` |  |
