# Verbatik: List My Voices

Retrieves your cloned voices from Verbatik.

```
GET https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-my-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verbatik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-my-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-my-voices?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "source_audio_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `last_used_at` | date |  |
| `name` | string |  |
| `preview_url` | string |  |
| `source_audio_url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Verbatik API, this operation is `GET /v1/my-voices` (base URL `https://api.verbatik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-voices.md) for the provider-specific parameters and requirements.

