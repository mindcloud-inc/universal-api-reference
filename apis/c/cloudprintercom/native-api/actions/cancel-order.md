# Cancel Order with Cloudprinter.com

Cancels an order in Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/orders/cancel`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Cancel Order](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#cancel-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Client order reference. |
