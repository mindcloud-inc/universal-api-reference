# Hireflix Universal API Examples

These examples use the MindCloud API key and Hireflix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Positions

Retrieves positions from Hireflix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-positions?${params}`, {
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
      "active": true,
      "archived": 1,
      "createdAt": 1,
      "description": "string",
      "expires": 1,
      "id": "string",
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "public": true,
      "retakes": 1,
      "timeToAnswer": 1,
      "timeToThink": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [List Positions action reference](actions/list-positions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hireflix/latest/actions/list-positions).

## Add Interview Comment

Creates an interview comment in Hireflix.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/add-interview-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/add-interview-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.comment": "string"
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
      "comments": [
        {
          "createdAt": 1,
          "id": "string",
          "updatedAt": 1,
          "value": "string"
        }
      ],
      "id": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Interview Comment action reference](actions/add-interview-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hireflix/latest/actions/add-interview-comment).
