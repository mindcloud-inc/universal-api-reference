# Salesmate Universal API Examples

These examples use the MindCloud API key and Salesmate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Active Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "imagePath": "string",
      "isActive": 1,
      "isCurrentUser": true,
      "lastName": "Chen",
      "mobile": "string",
      "name": "Ava Chen",
      "photo": "string",
      "seats": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Active Users action reference](actions/get-active-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesmate/latest/actions/get-active-users).

## Add Activity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "owner": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "owner": 1,
    "type": "string"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Activity action reference](actions/add-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesmate/latest/actions/add-activity).
