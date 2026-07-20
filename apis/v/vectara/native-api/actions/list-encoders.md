# List Encoders with Vectara

Retrieves the available encoders from Vectara.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/encoders`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Encoders](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Regex filter against encoder names and descriptions. |
| `limit` | query | `number` | no | Maximum number of encoders to return. |
| `page_key` | query | `string` | no | Cursor for the next page of encoders. |
