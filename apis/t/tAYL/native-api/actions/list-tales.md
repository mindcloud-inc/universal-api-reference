# List Tales with TAYL

## Endpoint

- **Method:** `GET`
- **Path:** `/tales`
- **Base URL:** `https://x.tayl.app`
- **Official documentation:** [List Tales](https://my.tayl.app/create/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tales to return. |
| `startAfter` | query | `string` | no | Pagination cursor or offset to start after. |
| `status` | query | `string` | no | Filter tales by processing status. |
