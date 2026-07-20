# Get Events with Cryptolens

Retrieves analytics events from Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ai/GetEvents`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Get Events](https://app.cryptolens.io/docs/api/v3/GetEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Limit` | query | `number` | no | Maximum number of events to return. |
| `StartingAfter` | query | `number` | no | Cursor for events after the given id. |
| `EndingBefore` | query | `number` | no | Cursor for events before the given id. |
| `Time` | query | `string` | no | Unix timestamp or JSON interval filter. |
| `ProductId` | query | `number` | no | Product ID to filter on. |
| `Key` | query | `string` | no | License key string to filter on. |
| `Metadata` | query | `string` | no | Metadata string to filter on. |
| `v` | query | `string` | no | Method version. |
