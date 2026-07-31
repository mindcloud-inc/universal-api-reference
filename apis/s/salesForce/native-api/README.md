# Salesforce: Native API Reference

A consolidated summary of Salesforce's API configuration and 22 documented operations.

- **API base URL:** `https://{companyDomainName}.my.salesforce.com`

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

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientName` | path | `string` | yes | Name of the client for the API subdomain |

## Pagination

Use `limit` in the request parameters to set the page size (default 25; accepted range 1–200). Use `offset` in the request parameters as the record offset.

## Retry behavior

Stop after 50 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST services/data/v62.0/sobjects/Account` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_account.htm) |
| [Create Customer](actions/create-customer.md) | `POST services/data/v62.0/sobjects/Contact` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_contact.htm) |
| [Create Order](actions/create-order.md) | `POST /services/data/v64.0/sobjects/Order` |  |
| [Create Order Item](actions/create-order-item.md) | `POST /services/data/v64.0/sobjects/OrderItem` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_orderitem.htm) |
| [Create Product](actions/create-product.md) | `POST /services/data/v64.0/sobjects/Product2` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_product2.htm) |
| [Create Record](actions/create-record.md) | `POST services/data/v61.0/sobjects/:objectId/` |  |
| [Delete Record](actions/delete-record.md) | `DELETE services/data/v61.0/sobjects/:objectId/:recordId` |  |
| [Find Product Offer by Product Code](actions/find-product-by-product-code.md) | `GET services/data/v61.0/query?q=SELECT+Id,+ProductCode,+UPC__c,+%28SELECT+Quantity__c,+Consumed_Quantity__c,+id,+Vendor_ID__c,+Vendor_Offer__c+FROM Offers__r%29+FROM+Product2+WHERE+ProductCode+=+':productcode'` |  |
| [Get Contact by Email](actions/get-contact-by-email.md) | `GET services/data/v61.0/query` |  |
| [Get Contacts](actions/get-contacts.md) | `GET services/data/v61.0/query?q=SELECT+Id,+FirstName,+LastName,+Title,+Email,+MobilePhone,+Department+FROM+Contact` |  |
| [Get Fulfillment Orders](actions/get-fulfillment-orders.md) | `GET services/data/v61.0/query` |  |
| [Find Order by OrderNumber](actions/get-order.md) | `GET services/data/v61.0/query?q=SELECT+Id+FROM+Order+WHERE+Customer_PO__c=':orderNumber'` |  |
| [Get Order Delivery Group](actions/get-order-delivery-group.md) | `GET services/data/v61.0/query` |  |
| [Get Order Delivery Method](actions/get-order-delivery-method.md) | `GET services/data/v61.0/query` |  |
| [List Pricebook](actions/list-pricebook.md) | `GET /services/data/v56.0/query?q=SELECT+Id,+Name,+IsActive,+IsArchived,+IsDeleted,+IsStandard,+LastReferencedDate,+ValidFrom,+ValidTo,+LastViewedDate,+Description+FROM+Pricebook2` |  |
| [List Pricebook Entry](actions/list-pricebook-entry.md) | `GET /services/data/v56.0/query?q=SELECT+Id,+Product2Id,+Pricebook2Id,+Name,+ActivePriceAdjustmentQuantity,+IsActive,+IsArchived,+ProductCode,+ProductSellingModelId,+UseStandardPrice,+UnitPrice+FROM+PricebookEntry` |  |
| [Org sObjects (Lookup)](actions/lookup-s-objects.md) | `GET services/data/v61.0/sobjects/` | [docs](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_describe.htm) |
| [Query (SOQL)](actions/query.md) | `GET services/data/v61.0/query` | [docs](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_select.htm) |
| [Query Order Items (test)](actions/query-order-items-test.md) | `GET services/data/v61.0/query` |  |
| [Update Order Items](actions/update-invoice.md) | `PATCH services/data/v61.0/sobjects/OrderItem/:id` |  |
| [Update Product](actions/update-product.md) | `PATCH /services/data/v64.0/sobjects/Product2/:id` | [docs](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_product2.htm) |
| [Update Record](actions/update-recordv2.md) | `PATCH services/data/v61.0/sobjects/:objectId/:recordId` |  |
