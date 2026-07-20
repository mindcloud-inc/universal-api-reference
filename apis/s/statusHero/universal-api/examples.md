# Status Hero Universal API Examples

These examples use the MindCloud API key and Status Hero connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List members



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-members?${params}`, {
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
      "absentDates": [
        "string"
      ],
      "id": "string",
      "role": "string",
      "slug": "string",
      "teamLead": true,
      "user": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List members action reference](actions/list-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/statusHero/latest/actions/list-members).

## Add member absence



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-member-absence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1e1a64b7-54e0-4f5f-a492-7edc28c86094",
  "date": "2026-12-31"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-member-absence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1e1a64b7-54e0-4f5f-a492-7edc28c86094",
    "date": "2026-12-31"
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
      "date": "2026-05-07T12:00:00.000Z",
      "member": {}
    }
  ],
  "meta": {}
}
```

See the full [Add member absence action reference](actions/add-member-absence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/statusHero/latest/actions/add-member-absence).
