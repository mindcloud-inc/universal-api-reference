# Bland AI: Number Details

Retrieves inbound number details from Bland AI.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/number-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/number-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/number-details?${params}`, {
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
      "background_track": "string",
      "created_at": "string",
      "fallback_number": "string",
      "max_duration": 1,
      "pathway_id": "string",
      "phone_number": "string",
      "prompt": "string",
      "voice_id": 1,
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background_track` | string |  |
| `created_at` | string |  |
| `fallback_number` | string |  |
| `max_duration` | number |  |
| `pathway_id` | string |  |
| `phone_number` | string |  |
| `prompt` | string |  |
| `voice_id` | number |  |
| `webhook` | string |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/inbound/{phone_number}` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/number-details.md) for the provider-specific parameters and requirements.

