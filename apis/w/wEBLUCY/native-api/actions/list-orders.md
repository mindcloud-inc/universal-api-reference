# List Orders with WEBLUCY

Retrieves orders from WEBLUCY.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [List Orders](https://websitebuilder.docs.apiary.io/#reference/orders/list/list-all-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at_max` | query | `string` | no | List only orders created before this Unix timestamp, inclusive. |
| `created_at_min` | query | `string` | no | List only orders created after this Unix timestamp, inclusive. |
