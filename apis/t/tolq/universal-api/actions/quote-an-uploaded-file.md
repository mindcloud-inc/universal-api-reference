# Tolq: Quote an Uploaded File

Creates a quote for an uploaded file in Tolq.

```
POST https://connect.mindcloud.co/v1/universal/tolq/latest/actions/quote-an-uploaded-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/quote-an-uploaded-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "a8d75d4706f38108d0dd86f7",
  "target_language_code": "de",
  "quality": "translation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolq/latest/actions/quote-an-uploaded-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "a8d75d4706f38108d0dd86f7",
    "target_language_code": "de",
    "quality": "translation"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Uploaded file UID returned by Initiate File Upload. Example: `a8d75d4706f38108d0dd86f7`. |
| `target_language_code` | string | yes | Two-letter ISO 639-1 target language code. Example: `de`. |
| `quality` | string | yes | Tolq quality level: machine, postediting, translation, localization, or expert. Example: `translation`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "quality": "string",
      "slug": "string",
      "source_language_code": "string",
      "status": "string",
      "style_guide_reference_id": 1,
      "target_language_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `completed_at` | date |  |
| `context_url` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `quality` | string |  |
| `slug` | string |  |
| `source_language_code` | string |  |
| `status` | string |  |
| `style_guide_reference_id` | number |  |
| `target_language_code` | string |  |

## Native endpoint

Through the native Tolq API, this operation is `POST /translations/requests/files/quote/:uid` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quote-an-uploaded-file.md) for the provider-specific parameters and requirements.

