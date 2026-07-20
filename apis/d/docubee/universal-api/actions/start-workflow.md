# Docubee: Start Workflow

Starts a workflow in Docubee.

```
POST https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/start-workflow', {
  method: 'POST',
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
| `body` | string | no | The workflow start payload. |
| `templateId` | string | no | The workflow template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "instanceId": "string",
      "startedOn": "string",
      "status": "string",
      "templateId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `instanceId` | string | The workflow instance ID. |
| `startedOn` | string | When the workflow instance started. |
| `status` | string | The workflow instance status. |
| `templateId` | string | The workflow template ID. |
| `tenantId` | string | The Docubee tenant ID. |

## Native endpoint

Through the native Docubee API, this operation is `POST /workflowTemplates/:templateId` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-workflow.md) for the provider-specific parameters and requirements.

