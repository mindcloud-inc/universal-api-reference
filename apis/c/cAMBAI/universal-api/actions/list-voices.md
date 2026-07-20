# CAMB.AI: List Voices

Retrieves all available voices from CAMB.AI.

```
GET https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/list-voices?${params}`, {
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
      "age": 1,
      "description": "string",
      "gender": 1,
      "id": 1,
      "import_counter": 1,
      "is_published": true,
      "language": 1,
      "owner": {},
      "owner_id": 1,
      "tags": [
        "string"
      ],
      "task_count": 1,
      "transcript": "string",
      "voice_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number | Approximate age metadata for the voice. |
| `description` | string | Description of the voice. |
| `gender` | number | Gender code for the voice. |
| `id` | number | Unique identifier for the voice. |
| `import_counter` | number | Internal import counter returned by CAMB.AI. |
| `is_published` | boolean | Whether the voice is published to the marketplace. |
| `language` | number | Language identifier associated with the voice. |
| `owner` | object | Owner details returned by CAMB.AI. |
| `owner_id` | number | Owner identifier for the voice. |
| `tags` | array<string> | Tags associated with the voice. |
| `task_count` | number | Internal task count returned by CAMB.AI. |
| `transcript` | string | Transcript used for the voice sample when available. |
| `voice_name` | string | Display name of the voice. |

## Native endpoint

Through the native CAMB.AI API, this operation is `GET /list-voices` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

