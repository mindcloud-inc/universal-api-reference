# Dungeon Fighter Online: Get Avatar Market Sale

Retrieves an avatar market listing from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sale?connectionId=$CONNECTION_ID&goodsNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goodsNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sale?${params}`, {
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
| `goodsNo` | number | yes | Avatar market goods number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": [
        {}
      ],
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
| `avatar` | array<object> |  |
| `avatarCount` | number |  |
| `avatarRarity` | string |  |
| `goodsNo` | number |  |
| `hashtag` | array<string> |  |
| `price` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/avatar-market/sale/:goodsNo` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-market-sale.md) for the provider-specific parameters and requirements.

