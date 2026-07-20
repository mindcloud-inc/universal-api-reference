# Dungeon Fighter Online: Get Avatar Market Sold Item

Retrieves sold avatar market pricing from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sold-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sold-item?connectionId=$CONNECTION_ID&goodsNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goodsNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-avatar-market-sold-item?${params}`, {
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
| `goodsNo` | number | yes | Sold avatar market goods number. |

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
| `avatar` | array<object> |  |
| `avatarCount` | number |  |
| `avatarRarity` | string |  |
| `goodsNo` | number |  |
| `hashtag` | array<string> |  |
| `price` | number |  |
| `soldDate` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/avatar-market/sold/:goodsNo` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-market-sold-item.md) for the provider-specific parameters and requirements.

