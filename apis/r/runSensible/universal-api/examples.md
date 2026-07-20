# RunSensible Universal API Examples

These examples use the MindCloud API key and RunSensible connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=c6aaa7ff-ff5e-45fe-bc53-973062b499c9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "c6aaa7ff-ff5e-45fe-bc53-973062b499c9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact?${params}`, {
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
      "communication": {
        "email": "ava@example.com"
      },
      "creationDate": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "owner": {
        "id": "string",
        "value": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Contact action reference](actions/get-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runSensible/latest/actions/get-contact).

## Complete Task



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/complete-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/complete-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Complete Task action reference](actions/complete-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runSensible/latest/actions/complete-task).
