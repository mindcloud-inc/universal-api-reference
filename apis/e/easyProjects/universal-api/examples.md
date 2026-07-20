# Easy Projects Universal API Examples

These examples use the MindCloud API key and Easy Projects connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves the current Easy Projects account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-current-account?${params}`, {
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
      "isHttpsForced": true,
      "mobileAppMenuItems": [
        {}
      ],
      "signIn": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyProjects/latest/actions/get-current-account).

## Add Task Message

Creates a new message on an Easy Projects task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/add-task-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123",
  "model": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/add-task-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123",
    "model": {}
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
      "id": 1,
      "messageText": "string",
      "postDate": "2026-05-07T12:00:00.000Z",
      "projectId": 1,
      "taskId": 1,
      "user": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Task Message action reference](actions/add-task-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyProjects/latest/actions/add-task-message).
