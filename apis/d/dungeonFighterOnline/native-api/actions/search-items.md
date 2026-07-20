# Search Items with Dungeon Fighter Online

Finds items in Dungeon Fighter Online by item name.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/items`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemName` | query | `string` | yes | Item name search term. |
| `limit` | query | `number` | no | Maximum number of items to return. |
