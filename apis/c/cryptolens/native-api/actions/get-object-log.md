# Get Object Log with Cryptolens

Retrieves object logs from Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ai/GetObjectLog`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Get Object Log](https://app.cryptolens.io/docs/api/v3/GetObjectLog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Limit` | query | `number` | no | Maximum number of object log entries to return. |
| `StartingAfter` | query | `number` | no | Cursor for object log entries after the given id. |
| `v` | query | `string` | no | Method version. |
