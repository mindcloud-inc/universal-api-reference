# Innform Universal API Examples

These examples use the MindCloud API key and Innform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Innform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-users?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/innform/latest/actions/list-users).

## Create Assignment

Assigns a training item to a user in Innform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/innform/latest/actions/create-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/innform/latest/actions/create-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "userId": "string"
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

See the full [Create Assignment action reference](actions/create-assignment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/innform/latest/actions/create-assignment).
