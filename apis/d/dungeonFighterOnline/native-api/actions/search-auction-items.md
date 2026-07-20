# Search Auction Items with Dungeon Fighter Online

Finds auction listings in Dungeon Fighter Online by item name.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/auction`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Auction Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemName` | query | `string` | yes | Auction item name search term. |
| `limit` | query | `number` | no | Maximum number of auction listings to return. |
