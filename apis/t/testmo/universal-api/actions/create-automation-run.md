# Testmo: Create Automation Run

Creates a new automation run in Testmo.

```
POST https://connect.mindcloud.co/v1/universal/testmo/latest/actions/create-automation-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/create-automation-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "name": "Ava Chen",
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testmo/latest/actions/create-automation-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "name": "Ava Chen",
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | ID of the target project. |
| `name` | string | yes | Name of the new automation run. |
| `source` | string | yes | Name of the automation source for the new run. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Testmo API returns.

## Native endpoint

Through the native Testmo API, this operation is `POST /projects/{project_id}/automation/runs` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-automation-run.md) for the provider-specific parameters and requirements.

