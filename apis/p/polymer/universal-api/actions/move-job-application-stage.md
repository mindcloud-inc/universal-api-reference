# Polymer: Move Job Application Stage

Moves a job application to a hiring stage in Polymer.

```
PUT https://connect.mindcloud.co/v1/universal/polymer/latest/actions/move-job-application-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polymer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/move-job-application-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polymer/latest/actions/move-job-application-stage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hiring_stage_id` | string | no | Target hiring stage ID for the job application's job. |
| `job_application_id` | string | no | Numeric Polymer job application ID. |
| `skip_message_automations` | string | no | Whether to skip message automations on the target stage. Must be a boolean. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Polymer API returns.

## Native endpoint

Through the native Polymer API, this operation is `POST /job_applications/:job_application_id/move_stage` (base URL `https://api.polymer.co/v1/hire`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-job-application-stage.md) for the provider-specific parameters and requirements.

