# Hume AI: List Voices

Retrieves voices from Hume AI.

```
GET https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-voices?connectionId=$CONNECTION_ID&provider=CUSTOM_VOICE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "provider": "CUSTOM_VOICE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-voices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `provider` | string | yes | Voice provider to list. Default: `CUSTOM_VOICE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNumber": 1,
      "pageSize": 1,
      "totalPages": 1,
      "voicesPage": [
        {}
      ],
      "voiceTagSummary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNumber` | number | Current page number. |
| `pageSize` | number | Current page size. |
| `totalPages` | number | Total number of pages. |
| `voicesPage` | array<object> | Voices returned for the current page. |
| `voiceTagSummary` | object | Tag summary for the returned voices. |

## Native endpoint

Through the native Hume AI API, this operation is `GET /v0/tts/voices` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

