# Unstructured: Update Workflow

Updates a workflow in Unstructured.

```
PUT https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-workflow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | The workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "destinationId": "string",
      "id": "string",
      "name": "Ava Chen",
      "sourceId": "string",
      "updatedAt": "string",
      "workflowNodes": [
        [
          {}
        ]
      ],
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `destinationId` | string | Destination connector ID. |
| `id` | string | Workflow ID. |
| `name` | string | Workflow name. |
| `sourceId` | string | Source connector ID. |
| `updatedAt` | string | Last update timestamp. |
| `workflowNodes[]` | array<object> | Workflow nodes. |
| `workflowType` | string | Workflow type. |

## Native endpoint

Through the native Unstructured API, this operation is `PUT /workflows/:workflow_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow.md) for the provider-specific parameters and requirements.

