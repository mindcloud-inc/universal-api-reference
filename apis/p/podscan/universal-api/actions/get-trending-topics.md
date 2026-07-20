# Podscan: Get Trending Topics

Retrieves trending topic results from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-trending-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-trending-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-trending-topics?${params}`, {
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
      "timeframe": "string",
      "topics": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timeframe` | string |  |
| `topics` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /topics/trending` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trending-topics.md) for the provider-specific parameters and requirements.

