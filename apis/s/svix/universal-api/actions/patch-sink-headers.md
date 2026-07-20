# Svix: Patch Sink Headers

Updates sink headers in Svix.

```
PUT https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-sink-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-sink-headers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/patch-sink-headers', {
  method: 'PUT',
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
      "headers": {},
      "sensitive": [
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
| `headers` | object |  |
| `sensitive` | array<string> |  |

## Native endpoint

Through the native Svix API, this operation is `PATCH /api/v1/stream/{stream_id}/sink/{sink_id}/headers` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-sink-headers.md) for the provider-specific parameters and requirements.

