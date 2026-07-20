# TeamBook Universal API Examples

These examples use the MindCloud API key and TeamBook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves all project records from TeamBook.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-projects?${params}`, {
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
      "active": "string",
      "business_unit": "string",
      "client_id": "string",
      "code": "string",
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": [
        [
          "string"
        ]
      ],
      "end_date": "2026-05-07T12:00:00.000Z",
      "estimated": "string",
      "id": "string",
      "kind": "string",
      "manager": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "notes": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamBook/latest/actions/list-projects).

## Create Actual Logs

Creates new actual logs in TeamBook.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-actual-logs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/create-actual-logs', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "id": "string",
      "payroll_item": {
        "id": 1,
        "name": "Ava Chen"
      },
      "project": {
        "code": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "task": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Actual Logs action reference](actions/create-actual-logs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teamBook/latest/actions/create-actual-logs).
