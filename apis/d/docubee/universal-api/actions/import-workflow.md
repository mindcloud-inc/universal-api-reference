# Docubee: Import Workflow

Imports a workflow into Docubee.

```
PUT https://connect.mindcloud.co/v1/universal/docubee/latest/actions/import-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/import-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/import-workflow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | The imported workflow template payload. |
| `fileContentBase64` | string | no | The exported workflow file content encoded as base64. |
| `publish` | string | no | Whether to publish the imported workflow immediately. Use true to make the template startable. |
| `templateId` | string | no | The workflow template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "published": true,
      "state": "string",
      "templateId": "string",
      "wfModelId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | The workflow template name. |
| `published` | boolean | Whether the workflow template is published. |
| `state` | string | The workflow template state. |
| `templateId` | string | The workflow template ID. |
| `wfModelId` | string | The workflow model ID. |

## Native endpoint

Through the native Docubee API, this operation is `PUT /workflowTemplates/:templateId` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-workflow.md) for the provider-specific parameters and requirements.

