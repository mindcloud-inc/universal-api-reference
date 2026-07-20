# Port API AI: Update Workflow

Updates a workflow in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowIdentifier": "string",
  "identifier": "string",
  "nodes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-workflow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowIdentifier": "string",
    "identifier": "string",
    "nodes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowIdentifier` | string | yes | The Port workflow identifier. |
| `identifier` | string | yes |  |
| `nodes[]` | array<object> | yes |  |
| `title` | string | no |  |
| `icon` | string | no |  |
| `connections[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `workflow` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `PUT /workflows/:workflow_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow.md) for the provider-specific parameters and requirements.

