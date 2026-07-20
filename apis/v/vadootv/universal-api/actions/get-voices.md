# Vadootv: Get voices

Retrieves available AI voices from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-voices?${params}`, {
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
      "": [
        {
          "accent": "string",
          "gender": "string",
          "name": "Ava Chen",
          "preview_url": "https://example.com",
          "voice_id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> | Available voice records. |
| `[].accent` | string | Voice accent. |
| `[].gender` | string | Voice gender. |
| `[].name` | string | Voice display name. |
| `[].preview_url` | string | Preview audio URL for the voice. |
| `[].voice_id` | string | Provider voice identifier. |

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_voices` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voices.md) for the provider-specific parameters and requirements.

