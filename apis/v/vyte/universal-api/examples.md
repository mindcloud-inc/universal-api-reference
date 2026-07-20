# Vyte Universal API Examples

These examples use the MindCloud API key and Vyte connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from Vyte.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-users?${params}`, {
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
      "_id": "string",
      "emails": [
        "ava@example.com"
      ],
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "last_name": "Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vyte/latest/actions/list-users).

## Book Event With Team Member

Books an event with a team member in Vyte.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/book-event-with-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vyte/latest/actions/book-event-with-team-member', {
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
      "_id": "string",
      "first_start_date": "string",
      "invitees_length": 1,
      "last_end_date": "string",
      "org": "string",
      "timezone": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Book Event With Team Member action reference](actions/book-event-with-team-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vyte/latest/actions/book-event-with-team-member).
