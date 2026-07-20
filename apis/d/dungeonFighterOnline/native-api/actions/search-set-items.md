# Search Set Items with Dungeon Fighter Online

Finds set items in Dungeon Fighter Online by set name.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/setitems`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Set Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setItemName` | query | `string` | yes | Set item name search term. |
| `limit` | query | `number` | no | Maximum number of set items to return. |
