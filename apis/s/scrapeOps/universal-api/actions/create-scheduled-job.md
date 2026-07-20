# ScrapeOps: Create Scheduled Job

Creates a scheduled job in ScrapeOps.

```
POST https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/create-scheduled-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/create-scheduled-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serverId": 1,
  "serverSpiderId": 1,
  "cronToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/create-scheduled-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serverId": 1,
    "serverSpiderId": 1,
    "cronToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | yes | The numeric ScrapeOps server id that owns the scheduled spider. |
| `serverSpiderId` | number | yes | The numeric spider id to schedule on the selected server. |
| `cronToken` | string | yes | The cron expression that controls when the job runs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `POST https://backend.scrapeops.io/v1/client/scheduled-jobs` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduled-job.md) for the provider-specific parameters and requirements.

