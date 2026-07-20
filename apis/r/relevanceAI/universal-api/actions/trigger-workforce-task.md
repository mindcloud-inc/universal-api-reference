# Relevance AI: Trigger Workforce Task



```
POST https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-workforce-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-workforce-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workforceId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/trigger-workforce-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workforceId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `role` | string | no | The role for the trigger message. Defaults to user. Default: `user`. |
| `workforceId` | string | yes | The workforce id to trigger. |
| `message` | string | yes | The user message to send to the workforce. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobs": {
        "job_info": {
          "job_id": "string",
          "studio_id": "string"
        },
        "node": {
          "node_id": "string",
          "type": "string"
        },
        "trigger_result": {
          "conversation_id": "string"
        }
      },
      "workforce_task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobs` | array<object> | The triggered workforce jobs. |
| `jobs.job_info.job_id` | string | The created job ID. |
| `jobs.job_info.studio_id` | string | The studio ID used for the job. |
| `jobs.node.node_id` | string | The triggered node ID. |
| `jobs.node.type` | string | The triggered node type. |
| `jobs.trigger_result.conversation_id` | string | The created conversation ID for the first triggered job. |
| `workforce_task_id` | string | The created workforce task ID. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /workforce/trigger` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-workforce-task.md) for the provider-specific parameters and requirements.

