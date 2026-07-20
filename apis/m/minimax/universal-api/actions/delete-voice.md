# Minimax: Delete Voice

Deletes a voice from Minimax.

```
DELETE https://connect.mindcloud.co/v1/universal/minimax/latest/actions/delete-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/delete-voice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/delete-voice?${params}`, {
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
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      },
      "created_time": "string",
      "description": "string",
      "voice_id": "string"
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
| `created_time` | string |  |
| `description` | string |  |
| `voice_id` | string |  |

## Native endpoint

Through the native Minimax API, this operation is `POST /v1/delete_voice` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-voice.md) for the provider-specific parameters and requirements.

