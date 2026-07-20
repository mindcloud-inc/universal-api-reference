# Add List Item with LEADTEX

Creates a new item in a LEADTEX list.

## Endpoint

- **Method:** `POST`
- **Path:** `/addListItem?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Add List Item](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Item fields object keyed by schema field slug. |
| `schema_id` | body | `string` | yes | ID of the list schema to add the item to. |
