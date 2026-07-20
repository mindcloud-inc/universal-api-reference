# Add List Item with Watbot

Creates a new list item in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/addListItem`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Add List Item](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema. |
| `data` | body | `object` | yes | List item field values. |
