# Port API AI: Create Workflow Node Permissions



```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow-node-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow-node-permissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nodeIdentifier": "string",
  "workflowIdentifier": "string",
  "read": true,
  "update": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow-node-permissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nodeIdentifier": "string",
    "workflowIdentifier": "string",
    "read": true,
    "update": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nodeIdentifier` | string | yes | The workflow node identifier. |
| `workflowIdentifier` | string | yes | The workflow identifier. |
| `read` | boolean | yes | Whether the node can be viewed. |
| `update` | boolean | yes | Whether the node can be updated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /workflows/:workflow_identifier/nodes/:node_identifier/permissions` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow-node-permissions.md) for the provider-specific parameters and requirements.

