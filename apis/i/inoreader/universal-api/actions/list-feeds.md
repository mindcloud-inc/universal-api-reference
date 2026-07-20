# Inoreader: List Feeds

Retrieves feed subscriptions from Inoreader.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-feeds?${params}`, {
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
      "subscriptions": [
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
| `subscriptions` | array<object> | The subscriptions returned by Inoreader for the connected account. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /subscription/list` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feeds.md) for the provider-specific parameters and requirements.

