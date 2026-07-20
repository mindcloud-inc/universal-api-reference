# Wrangle: Start Workflow



```
POST https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/start-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/start-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "workflow_uuid",
  "requesterId": "U12345678",
  "formFieldValues[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/start-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "workflow_uuid",
    "requesterId": "U12345678",
    "formFieldValues[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | The Wrangle workflow ID to start. Example: `workflow_uuid`. |
| `requesterId` | string | yes | The Slack user ID of the user starting the workflow instance. Example: `U12345678`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formFieldValues[]` | array<object> | yes | Workflow intake form values. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wrangle API returns.

## Native endpoint

Through the native Wrangle API, this operation is `POST /workflows/:workflowId/instances` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-workflow.md) for the provider-specific parameters and requirements.

