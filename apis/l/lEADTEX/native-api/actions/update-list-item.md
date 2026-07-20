# Update List Item with LEADTEX

Updates an existing item in a LEADTEX list.

## Endpoint

- **Method:** `POST`
- **Path:** `/updateListItem?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Update List Item](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Updated item fields object keyed by schema field slug. |
| `item_id` | body | `string` | yes | ID of the list item to update. |
