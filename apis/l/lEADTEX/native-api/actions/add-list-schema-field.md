# Add List Schema Field with LEADTEX

Creates a new field in a LEADTEX list schema.

## Endpoint

- **Method:** `POST`
- **Path:** `/addListSchemaField?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Add List Schema Field](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | body | `object` | yes | Field definition object to add. |
| `schema_id` | body | `string` | yes | ID of the list schema to add the field to. |
