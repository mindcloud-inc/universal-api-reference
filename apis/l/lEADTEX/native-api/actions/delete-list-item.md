# Delete List Item with LEADTEX

Deletes an existing item from a LEADTEX list.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteListItem?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Delete List Item](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | body | `string` | yes | ID of the list item to delete. |
