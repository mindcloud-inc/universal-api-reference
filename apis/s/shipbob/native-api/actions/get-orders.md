# Get Orders with ShipBob

## Endpoint

- **Method:** `GET`
- **Path:** `2026-07/order`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST
- **Official documentation:** [Get Orders](https://developer.shipbob.com/api/2025-07/orders/get-orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StartDate` | query | `string` | no | — |
| `IDs` | query | `string<string>` | no | Send multiple values as a array. |
| `HasTracking` | query | `string` | no | — |
| `isTrackingUploaded` | query | `string` | no | — |
