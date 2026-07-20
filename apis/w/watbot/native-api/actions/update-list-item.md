# Update List Item with Watbot

Updates an existing list item in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/updateListItem`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Update List Item](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema. |
| `item_id` | body | `string` | yes | ID of the list item. |
| `data` | body | `object` | yes | Updated list item values. |
