# Webpushr: Get Subscriber Count



```
GET https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webpushr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count?${params}`, {
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
      "activeSubscribers": "string",
      "totalLifeTimeSubscribers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSubscribers` | string | Active subscribers for the site. |
| `totalLifeTimeSubscribers` | string | Total lifetime subscribers for the site. |

## Native endpoint

Through the native Webpushr API, this operation is `GET /site/subscriber_count` (base URL `https://api.webpushr.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-count.md) for the provider-specific parameters and requirements.

