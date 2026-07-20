# Cancel Shipment with Easyship

Cancels a shipment in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:shipment_id/cancel`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Cancel Shipment](https://developers.easyship.com/reference/shipments_cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_id` | path | `string` | yes | The Easyship shipment ID. |
