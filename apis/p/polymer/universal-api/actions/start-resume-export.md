# Polymer: Start Resume Export

Starts a resume export job in Polymer.

```
POST https://connect.mindcloud.co/v1/universal/polymer/latest/actions/start-resume-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polymer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/polymer/latest/actions/start-resume-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polymer/latest/actions/start-resume-export', {
  method: 'POST',
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
| `job_id` | string | no | Numeric Polymer job ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Polymer API returns.

## Native endpoint

Through the native Polymer API, this operation is `POST /jobs/:job_id/resume_export_job` (base URL `https://api.polymer.co/v1/hire`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-resume-export.md) for the provider-specific parameters and requirements.

