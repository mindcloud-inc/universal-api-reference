# Testmo: Complete Automation Run

Marks an automation run as completed in Testmo.

```
PUT https://connect.mindcloud.co/v1/universal/testmo/latest/actions/complete-automation-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/complete-automation-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "automationRunId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testmo/latest/actions/complete-automation-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "automationRunId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `automationRunId` | number | yes | ID of the automation run to complete. |
| `measureElapsed` | boolean | no | Whether Testmo should compute elapsed time from run creation to completion. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Testmo API returns.

## Native endpoint

Through the native Testmo API, this operation is `POST /automation/runs/{automation_run_id}/complete` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-automation-run.md) for the provider-specific parameters and requirements.

