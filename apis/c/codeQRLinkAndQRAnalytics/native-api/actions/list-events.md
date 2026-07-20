# List Events with CodeQR - Link and QR Analytics

Retrieves events from CodeQR.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [List Events](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | query | `string` | no | The type of event to retrieve. |
| `interval` | query | `string` | no | The interval to retrieve events for. |
| `page` | query | `number` | no | The page number for events pagination. |
| `limit` | query | `number` | no | The number of events to return. |
