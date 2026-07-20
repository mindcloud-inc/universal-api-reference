# List Item Fulfillments with NetSuite - Advanced

Item Fulfillment is a record that says, “We shipped these items to the customer.” It’s how NetSuite keeps track of what was sent out from a sales order.

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST
- **Official documentation:** [List Item Fulfillments](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/itemfulfillment.html)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `object` | no | — |
| `includeAllSublists` | body | `boolean` | no | Format: `toggle`. |
