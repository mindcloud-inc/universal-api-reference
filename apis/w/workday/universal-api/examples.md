# Workday Universal API Examples

These examples use the MindCloud API key and Workday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workers

List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workday/latest/actions/get-workers?${params}`, {
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
      "additionalJobs": [
        {}
      ],
      "descriptor": "string",
      "id": "string",
      "person": {},
      "primaryJob": {},
      "workerId": "string",
      "workerType": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Workers action reference](actions/get-workers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workday/latest/actions/get-workers).

## Create Timesheet Entry

Create a worker time block in Workday Time Tracking for a specific worker using either quantity-based or clock-in and clock-out entry fields.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workday/latest/actions/create-timesheet-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workday/latest/actions/create-timesheet-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workerId": "string"
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

See the full [Create Timesheet Entry action reference](actions/create-timesheet-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workday/latest/actions/create-timesheet-entry).
