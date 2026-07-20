# IceCubes Universal API Examples

These examples use the MindCloud API key and IceCubes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-user?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "meetingCount": 1,
      "organizationId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iceCubes/latest/actions/get-user).

## Create Action Item



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/create-action-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/create-action-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingId": "string",
    "text": "string"
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
      "assigneeEmail": "ava@example.com",
      "completed": true,
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "meetingId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Action Item action reference](actions/create-action-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iceCubes/latest/actions/create-action-item).
