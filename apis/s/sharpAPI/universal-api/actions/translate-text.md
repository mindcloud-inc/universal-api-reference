# SharpAPI: Translate Text

Creates a text translation job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Paste the text you want translated.",
  "language": "German"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Paste the text you want translated.",
    "language": "German"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Content to translate. Example: `Paste the text you want translated.`. |
| `language` | string | yes | Target language for the translated output. Example: `German`. |
| `voiceTone` | string | no | Preferred tone of the translated output. Example: `Professional`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | string | no | Additional processing instructions for the translation. Example: `Keep product names in English.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "status_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | SharpAPI job identifier. |
| `status_url` | string | Job status URL returned by SharpAPI. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /content/translate` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-text.md) for the provider-specific parameters and requirements.

