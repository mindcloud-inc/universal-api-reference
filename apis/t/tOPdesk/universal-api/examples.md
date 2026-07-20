# TOPdesk Universal API Examples

These examples use the MindCloud API key and TOPdesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Incident Statuses

Retrieves available incident statuses from TOPdesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/list-incident-statuses?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Incident Statuses action reference](actions/list-incident-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tOPdesk/latest/actions/list-incident-statuses).

## Add Incident Time Spent

Creates a time spent entry for an incident in TOPdesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/add-incident-time-spent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "timeSpent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/add-incident-time-spent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "timeSpent": 1
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "entryDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "notes": "string",
      "status": 1,
      "timeSpent": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Incident Time Spent action reference](actions/add-incident-time-spent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tOPdesk/latest/actions/add-incident-time-spent).
