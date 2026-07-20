# Delete List Item with Watbot

Deletes an existing list item from Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteListItem`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Delete List Item](https://docs.watbot.ru/rabota-s-api/spiski/elementy-spiska)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | body | `string` | yes | ID of the list item. |
