# Delete List Schema Field with Watbot

Deletes a list schema field from Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteListSchemaField`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Delete List Schema Field](https://docs.watbot.ru/rabota-s-api/spiski/spiski)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | body | `string` | yes | Slug of the field to delete. |
| `schema_id` | body | `string` | yes | ID of the list schema. |
