# Dungeon Fighter Online: Search Avatar Market Sold Items

Finds sold avatar market listings in Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sold-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sold-items?connectionId=$CONNECTION_ID&hashtag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hashtag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sold-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hashtag` | string | yes | Sold avatar market hashtag search term. |
| `limit` | number | no | Maximum number of sold avatar market records to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarCount": 1,
      "avatarRarity": "string",
      "goodsNo": 1,
      "hashtag": [
        "string"
      ],
      "price": 1,
      "soldDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarCount` | number |  |
| `avatarRarity` | string |  |
| `goodsNo` | number |  |
| `hashtag` | array<string> |  |
| `price` | number |  |
| `soldDate` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/avatar-market/sold` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-avatar-market-sold-items.md) for the provider-specific parameters and requirements.

