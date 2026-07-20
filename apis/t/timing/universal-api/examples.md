# Timing Universal API Examples

These examples use the MindCloud API key and Timing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves all project records from Timing.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timing/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timing/latest/actions/list-projects?${params}`, {
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
      "children": [
        {}
      ],
      "color": "string",
      "customFields": {},
      "defaultBillingStatus": "string",
      "isArchived": true,
      "notes": "string",
      "parent": {
        "self": "string"
      },
      "productivityScore": 1,
      "self": "string",
      "teamId": "string",
      "title": "string",
      "titleChain": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timing/latest/actions/list-projects).

## Batch Update Time Entries

Updates multiple time entries at once in Timing.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timing/latest/actions/batch-update-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntries[]": [
    "string"
  ],
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timing/latest/actions/batch-update-time-entries', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeEntries[]": ["string"],
    "data": {}
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
      "billingStatus": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "customFields": {},
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "isRunning": true,
      "notes": "string",
      "project": {
        "self": "string"
      },
      "self": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Update Time Entries action reference](actions/batch-update-time-entries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timing/latest/actions/batch-update-time-entries).
