# SharpAPI: Generate Keywords Tags

Creates keywords and tags in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-keywords-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-keywords-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Paste the text you want tagged."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-keywords-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Paste the text you want tagged."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Content to analyze for keywords and tags. Example: `Paste the text you want tagged.`. |
| `language` | string | no | Language for the generated keywords and tags. Default: `English`. Example: `English`. |
| `maxQuantity` | number | no | Maximum number of keywords to generate. Example: `10`. |
| `voiceTone` | string | no | Preferred tone for keyword generation. Example: `Neutral`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | string | no | Additional instructions for keyword generation. Example: `Focus on software integration and automation terms.`. |

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

Through the native SharpAPI API, this operation is `POST /content/keywords` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-keywords-tags.md) for the provider-specific parameters and requirements.

