# Get External Order with Fourthwall

Retrieves an external order from Fourthwall by source and ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-api/v1.0/external-orders/:externalSource/:externalOrderId`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [Get External Order](https://docs.fourthwall.com/api-reference/platform/external-orders/get-external-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalSource` | path | `string` | yes | The external order source. |
| `externalOrderId` | path | `string` | yes | The external order ID. |
