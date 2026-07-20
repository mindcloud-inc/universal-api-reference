# Delete List Schema with LEADTEX

Deletes a list schema from LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteListSchema?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete List Schema](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema to delete. |
