# Dungeon Fighter Online: Search Avatar Market Sales

Finds avatar market listings in Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sales?connectionId=$CONNECTION_ID&hashtag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hashtag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/search-avatar-market-sales?${params}`, {
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
| `hashtag` | string | yes | Avatar market hashtag search term. |
| `limit` | number | no | Maximum number of avatar market sale listings to return. Default: `5`. |

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
| `title` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/avatar-market/sale` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-avatar-market-sales.md) for the provider-specific parameters and requirements.

