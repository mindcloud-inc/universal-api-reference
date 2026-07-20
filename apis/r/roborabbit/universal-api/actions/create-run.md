# Roborabbit: Create Run

Creates a new run for a Roborabbit task.

```
POST https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/create-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roborabbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/create-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/create-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | no | Optional metadata to store with the run. |
| `steps[]` | array<object> | no | Optional array of step override objects for this run. |
| `steps[].action` | string | no | The action name for the step override. |
| `steps[].config` | object | no | The config object for the step override. |
| `steps[].skip` | boolean | no | Set true to skip this step for the run. |
| `steps[].uid` | string | no | The UID of the task step to override. |
| `taskUid` | string | yes | The task UID to execute. |
| `webhookUrl` | string | no | Optional URL to receive the completed run object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedInSeconds": 1,
      "metadata": "string",
      "outputs": [
        "string"
      ],
      "status": "string",
      "steps": [
        {}
      ],
      "task": "string",
      "uid": "string",
      "videoUrl": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `finishedInSeconds` | number |  |
| `metadata` | string |  |
| `outputs` | array |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `task` | string |  |
| `uid` | string |  |
| `videoUrl` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Roborabbit API, this operation is `POST /v1/tasks/:task_uid/runs` (base URL `https://api.roborabbit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-run.md) for the provider-specific parameters and requirements.

