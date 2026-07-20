# Blip: Associate Answer to Intent

Associates an answer with an intent in Blip.

```
POST https://connect.mindcloud.co/v1/universal/blip/latest/actions/associate-answer-to-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blip/latest/actions/associate-answer-to-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blip/latest/actions/associate-answer-to-intent', {
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
      "from": "string",
      "id": "string",
      "metadata": {},
      "method": "string",
      "resource": {},
      "status": "string",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string | BLiP source node. |
| `id` | string | BLiP command identifier. |
| `metadata` | object | BLiP command response metadata. |
| `method` | string | BLiP command method echoed by the provider. |
| `resource` | object | BLiP command response resource payload when present. |
| `status` | string | BLiP command execution status. |
| `to` | string | BLiP destination node. |
| `type` | string | BLiP command response content type. |

## Native endpoint

Through the native Blip API, this operation is `POST /commands` (base URL `https://ae2bd556-b116-4f7a-a0d3-30a54ef5b9d7.http.msging.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/associate-answer-to-intent.md) for the provider-specific parameters and requirements.

