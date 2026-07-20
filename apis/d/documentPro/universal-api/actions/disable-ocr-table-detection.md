# DocumentPro: Disable OCR Table Detection

Disables OCR table detection for a DocumentPro workflow.

```
PUT https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/disable-ocr-table-detection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/disable-ocr-table-detection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/disable-ocr-table-detection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template_id` | string | yes | The workflow template_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "email_id": "ava@example.com",
      "parser_config": {},
      "template_id": "string",
      "template_schema": {},
      "template_title": "string",
      "template_type": "string",
      "user_id": "string",
      "version": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email_id` | string |  |
| `parser_config` | object |  |
| `template_id` | string |  |
| `template_schema` | object |  |
| `template_title` | string |  |
| `template_type` | string |  |
| `user_id` | string |  |
| `version` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native DocumentPro API, this operation is `PUT /v1/templates/:template_id` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-ocr-table-detection.md) for the provider-specific parameters and requirements.

