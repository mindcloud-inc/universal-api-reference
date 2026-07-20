# Create Item Fulfillment with NetSuite - Advanced

Item Fulfillment is a record that says, “We shipped these items to the customer.” It’s how NetSuite keeps track of what was sent out from a sales order.

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `columns` | body | `object` | no |
