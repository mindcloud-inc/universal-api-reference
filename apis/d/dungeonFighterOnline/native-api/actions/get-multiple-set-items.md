# Get Multiple Set Items with Dungeon Fighter Online

Retrieves details for multiple set items from Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/multi/setitems`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Get Multiple Set Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setItemIds` | query | `string` | yes | Comma-separated Dungeon Fighter set item IDs. |
