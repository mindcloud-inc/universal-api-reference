# Get Multiple Items with Dungeon Fighter Online

Retrieves details for multiple items from Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/multi/items`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Get Multiple Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemIds` | query | `string` | yes | Comma-separated Dungeon Fighter item IDs. |
