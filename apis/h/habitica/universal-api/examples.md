# Habitica Universal API Examples

These examples use the MindCloud API key and Habitica connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the current user from Habitica.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-user?${params}`, {
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
      "appVersion": "string",
      "id": "string",
      "items": {},
      "notifications": [
        {}
      ],
      "preferences": {},
      "profile": {},
      "stats": {},
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/habitica/latest/actions/get-user).

## Add Checklist Item

Adds a checklist item to a Habitica task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/add-checklist-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/habitica/latest/actions/add-checklist-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
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
      "checklist": [
        {}
      ],
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "notes": "string",
      "priority": 1,
      "tags": [
        "string"
      ],
      "text": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Checklist Item action reference](actions/add-checklist-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/habitica/latest/actions/add-checklist-item).
