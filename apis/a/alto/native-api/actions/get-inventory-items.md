# Get Inventory Items with Alto

Retrieves inventory items from Alto by IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/items`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Inventory Items](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventory-id` | query | `string` | yes | Inventory item identifier to retrieve. The endpoint accepts one or more inventory IDs. Send multiple values as a string separated by `,`. |
