# Allscreenshots Universal API Examples

These examples use the MindCloud API key and Allscreenshots connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Schedules

Retrieves recurring screenshot schedules from Allscreenshots.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/list-schedules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextRunAt": "2026-05-07T12:00:00.000Z",
      "schedule": "string",
      "scheduleId": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Schedules action reference](actions/list-schedules.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/allscreenshots/latest/actions/list-schedules).

## Create Async Screenshot Job

Creates a new async screenshot job in Allscreenshots.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-async-screenshot-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-async-screenshot-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Async Screenshot Job action reference](actions/create-async-screenshot-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/allscreenshots/latest/actions/create-async-screenshot-job).
