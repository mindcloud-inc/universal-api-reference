# Get Multiple Warehouse Receiving Orders with ShipBob

## Endpoint

- **Method:** `GET`
- **Path:** `2026-07/receiving`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrderNumbers` | query | `string` | no | Send multiple values as a array. |
| `Statuses` | query | `list` | no | Send multiple values as a array separated by `false`. |
| `ids[]` | query | `array<string>` | no | — |
