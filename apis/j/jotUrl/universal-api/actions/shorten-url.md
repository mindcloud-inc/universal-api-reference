# JotUrl: Shorten URL

Creates a new tracking link in JotUrl.

```
POST https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/shorten-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JotUrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/shorten-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/shorten-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `status` | object |  |

## Native endpoint

Through the native JotUrl API, this operation is `POST /urls/shorten` (base URL `https://joturl.com/a/i1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shorten-url.md) for the provider-specific parameters and requirements.

