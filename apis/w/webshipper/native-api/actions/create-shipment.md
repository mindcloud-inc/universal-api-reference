# Create Shipment with Webshipper

Creates a shipment in Webshipper.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Create Shipment](https://docs.webshipper.io/#shipments)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.relationships.order.data.id` | body | `string` | yes | Order ID to create the shipment from. |
