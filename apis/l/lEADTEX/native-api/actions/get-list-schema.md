# Get List Schema with LEADTEX

Retrieves a specific list schema from LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getListSchema?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Get List Schema](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | query | `string` | yes | ID of the list schema to retrieve. |
