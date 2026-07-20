# ActiveMerge: Generate Workflow Documents

Generates documents from a workflow in ActiveMerge.

```
POST https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/generate-workflow-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/generate-workflow-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "[object Object]",
  "format": "pdf",
  "workflowId": "workflow_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/generate-workflow-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "[object Object]",
    "format": "pdf",
    "workflowId": "workflow_abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Object mapping workflow placeholders to values. Example: `[object Object]`. |
| `format` | string | yes | Output format: pdf, docx, or pptx. One of: `0`, `1`, `2`. Default: `pdf`. |
| `workflowId` | string | yes | Workflow ID to generate from. Example: `workflow_abc123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveMerge API returns.

## Native endpoint

Through the native ActiveMerge API, this operation is `POST /api/workflows/generate` (base URL `https://app.activemerge.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-workflow-documents.md) for the provider-specific parameters and requirements.

