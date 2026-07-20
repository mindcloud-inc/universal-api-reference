# Dungeon Fighter Online: List Item Hashtags

Retrieves item hashtags from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-item-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-item-hashtags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-item-hashtags?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<string> |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/item-hashtag` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-hashtags.md) for the provider-specific parameters and requirements.

