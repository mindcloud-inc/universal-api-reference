# QStash Universal API Examples

These examples use the MindCloud API key and QStash connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Schedules

Retrieves all existing schedules from QStash.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules?${params}`, {
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
      "body": "string",
      "callerIP": "string",
      "createdAt": 1,
      "cron": "string",
      "destination": "string",
      "header": {},
      "isPaused": true,
      "method": "string",
      "parallelism": 1,
      "retries": 1,
      "scheduleId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Schedules action reference](actions/list-schedules.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qStash/latest/actions/list-schedules).

## Add URL Group Endpoints

Adds endpoints to a QStash URL Group, creating it if needed.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/add-url-group-endpoints" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlGroupName": "https://example.com",
  "endpoints[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/add-url-group-endpoints', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlGroupName": "https://example.com",
    "endpoints[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add URL Group Endpoints action reference](actions/add-url-group-endpoints.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qStash/latest/actions/add-url-group-endpoints).
