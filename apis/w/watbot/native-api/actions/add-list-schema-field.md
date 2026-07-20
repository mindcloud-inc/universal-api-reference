# Add List Schema Field with Watbot

Adds a field to a list schema in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/addListSchemaField`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Add List Schema Field](https://docs.watbot.ru/rabota-s-api/spiski/spiski)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | body | `object` | yes | Field definition object. |
| `schema_id` | body | `string` | yes | ID of the list schema. |
