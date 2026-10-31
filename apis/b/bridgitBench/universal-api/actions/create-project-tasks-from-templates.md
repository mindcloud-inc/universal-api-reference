# Bridgit Bench: Create Project Tasks from Templates



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-tasks-from-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-tasks-from-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "projectId": 1,
  "payload[]": [
    {}
  ],
  "payload[].templateId": "string",
  "payload[].startDate": "2026-05-07T12:00:00.000Z",
  "payload[].endDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project-tasks-from-templates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "projectId": 1,
    "payload[]": [{}],
    "payload[].templateId": "string",
    "payload[].startDate": "2026-05-07T12:00:00.000Z",
    "payload[].endDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `projectId` | number | yes | The project ID the tasks belongs to |
| `payload[]` | array<object> | yes |  |
| `payload[].templateId` | string | yes |  |
| `payload[].startDate` | date | yes |  |
| `payload[].endDate` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/by-templates` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-tasks-from-templates.md) for the provider-specific parameters and requirements.

