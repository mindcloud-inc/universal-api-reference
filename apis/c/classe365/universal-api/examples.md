# Classe365 Universal API Examples

These examples use the MindCloud API key and Classe365 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Academic Sessions

Retrieves a list of academic sessions from Classe365.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/list-academic-sessions?${params}`, {
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
      "academicSessionId": "string",
      "academicSessionName": "Ava Chen",
      "endDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Academic Sessions action reference](actions/list-academic-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classe365/latest/actions/list-academic-sessions).

## Change Student Status

Updates a student's status in Classe365.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/change-student-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/change-student-status', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "studentIds": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Student Status action reference](actions/change-student-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/classe365/latest/actions/change-student-status).
