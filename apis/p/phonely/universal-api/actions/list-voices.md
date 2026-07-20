# Phonely: List Voices

Retrieves voices from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/list-voices?${params}`, {
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
      "accent": "string",
      "gender": "string",
      "id": "string",
      "isMultiLingualSupport": true,
      "language": "string",
      "name": "Ava Chen",
      "tags": [
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
| `accent` | string | Voice accent, when available. |
| `gender` | string | Voice gender label, when available. |
| `id` | string | Voice ID. |
| `isMultiLingualSupport` | boolean | Whether the voice supports multiple languages. |
| `language` | string | Primary voice language. |
| `name` | string | Voice display name. |
| `tags` | array<string> | Voice tags and provider labels. |

## Native endpoint

Through the native Phonely API, this operation is `GET /api/list-voices` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

