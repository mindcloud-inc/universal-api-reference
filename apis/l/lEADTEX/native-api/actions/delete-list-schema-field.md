# Delete List Schema Field with LEADTEX

Deletes a field from a LEADTEX list schema.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteListSchemaField?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete List Schema Field](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema containing the field. |
| `slug` | body | `string` | yes | Slug of the field to delete. |
