# Minimax: Lyrics Generation

Creates song lyrics in Minimax.

```
POST https://connect.mindcloud.co/v1/universal/minimax/latest/actions/lyrics-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/lyrics-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minimax/latest/actions/lyrics-generation', {
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
      }
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

## Native endpoint

Through the native Minimax API, this operation is `POST /v1/lyrics_generation` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lyrics-generation.md) for the provider-specific parameters and requirements.

