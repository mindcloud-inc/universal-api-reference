# Segmind: Run Flux Kontext Max



```
POST https://connect.mindcloud.co/v1/universal/segmind/latest/actions/run-flux-kontext-max
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Segmind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/run-flux-kontext-max" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/segmind/latest/actions/run-flux-kontext-max', {
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
      "metadata": {},
      "outputUrl": "https://example.com",
      "outputUrls": [
        "https://example.com"
      ],
      "requestId": "string",
      "status": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `outputUrl` | string |  |
| `outputUrls` | array<string> |  |
| `requestId` | string |  |
| `status` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Segmind API, this operation is `POST /v1/flux-kontext-max` (base URL `https://api.segmind.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-flux-kontext-max.md) for the provider-specific parameters and requirements.

