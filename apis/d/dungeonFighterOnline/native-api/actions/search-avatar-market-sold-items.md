# Search Avatar Market Sold Items with Dungeon Fighter Online

Finds sold avatar market listings in Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/avatar-market/sold`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Avatar Market Sold Items](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hashtag` | query | `string` | yes | Sold avatar market hashtag search term. |
| `limit` | query | `number` | no | Maximum number of sold avatar market records to return. |
