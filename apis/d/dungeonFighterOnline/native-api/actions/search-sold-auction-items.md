# Search Sold Auction Items with Dungeon Fighter Online

Finds sold auction listings in Dungeon Fighter Online by item name.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/auction-sold`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Sold Auction Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemName` | query | `string` | yes | Sold auction item name search term. |
| `limit` | query | `number` | no | Maximum number of sold auction records to return. |
