# Minimax: Voice Clone

Creates a cloned voice in Minimax.

```
POST https://connect.mindcloud.co/v1/universal/minimax/latest/actions/voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minimax/latest/actions/voice-clone', {
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
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      },
      "demo_audio": "string",
      "input_sensitive": true,
      "input_sensitive_type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_resp` | object |  |
| `base_resp.status_code` | number |  |
| `base_resp.status_msg` | string |  |
| `demo_audio` | string |  |
| `input_sensitive` | boolean |  |
| `input_sensitive_type` | number |  |

## Native endpoint

Through the native Minimax API, this operation is `POST /v1/voice_clone` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-clone.md) for the provider-specific parameters and requirements.

