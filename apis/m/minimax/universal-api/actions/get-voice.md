# Minimax: Get Voice

Retrieves available voices from Minimax.

```
GET https://connect.mindcloud.co/v1/universal/minimax/latest/actions/get-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minimax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/get-voice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/get-voice?${params}`, {
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
      "music_generation": "string",
      "system_voice": "string",
      "voice_cloning": "string",
      "voice_generation": "string",
      "voice_slots": "string"
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
| `music_generation` | string |  |
| `system_voice` | string |  |
| `voice_cloning` | string |  |
| `voice_generation` | string |  |
| `voice_slots` | string |  |

## Native endpoint

Through the native Minimax API, this operation is `POST /v1/get_voice` (base URL `https://api.minimax.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice.md) for the provider-specific parameters and requirements.

