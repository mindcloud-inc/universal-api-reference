# Search Nearby Events with Belong

Finds nearby events in Belong by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/nearby`
- **Base URL:** `https://api.belong.net/api/v3`
- **Official documentation:** [Search Nearby Events](https://api.belong.net/api/v3/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | — |
| `lng` | query | `number` | yes | — |
| `hubId` | query | `string` | no | — |
| `category[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `online` | query | `boolean` | no | — |
| `private` | query | `boolean` | no | — |
| `start` | query | `date` | no | — |
| `end` | query | `date` | no | — |
| `search` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `limit` | query | `number` | no | — |
