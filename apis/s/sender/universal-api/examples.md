# Sender Universal API Examples

These examples use the MindCloud API key and Sender connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Fields



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields?${params}`, {
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
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "default": true,
      "defaultValue": "string",
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "position": 1,
      "show": true,
      "title": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Fields action reference](actions/list-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sender/latest/actions/list-fields).

## Add Subscriber to Group



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sender/latest/actions/add-subscriber-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "grp_123",
  "subscribers[]": "user@example.com,another@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/add-subscriber-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "grp_123",
    "subscribers[]": "user@example.com,another@example.com"
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
      "message": {
        "nonExistingSubscribers": [
          "string"
        ],
        "subscribersAddedToGroup": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber to Group action reference](actions/add-subscriber-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sender/latest/actions/add-subscriber-to-group).
