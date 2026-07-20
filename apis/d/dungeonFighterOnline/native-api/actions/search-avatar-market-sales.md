# Search Avatar Market Sales with Dungeon Fighter Online

Finds avatar market listings in Dungeon Fighter Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/df/avatar-market/sale`
- **Base URL:** `https://api.neople.co.kr`
- **Official documentation:** [Search Avatar Market Sales](https://developers.neople.co.kr/contents/apiDocs/df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hashtag` | query | `string` | yes | Avatar market hashtag search term. |
| `limit` | query | `number` | no | Maximum number of avatar market sale listings to return. |
