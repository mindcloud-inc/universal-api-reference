# DocumentPro: Create Workflow

Creates a new workflow in DocumentPro.

```
POST https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parser_config` | object | no | Parser configuration object for email, OCR, and query settings. |
| `template_schema` | object | no | Template schema object describing extracted fields. |
| `template_title` | string | yes | Human-readable title for the workflow. |
| `template_type` | string | no | Optional workflow type label. |
| `webhook_url` | string | no | Optional webhook URL for workflow callbacks. |

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

Through the native DocumentPro API, this operation is `POST /v1/templates` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

