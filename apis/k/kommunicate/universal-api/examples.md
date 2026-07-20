# Kommunicate Universal API Examples

These examples use the MindCloud API key and Kommunicate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Detail

Retrieves user details from Kommunicate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userIdList%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdList[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail?${params}`, {
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
      "connected": true,
      "createdAtTime": 1,
      "deactivated": true,
      "displayName": "Ava Chen",
      "lastMessageAtTime": 1,
      "metadata": {},
      "roleType": 1,
      "unreadCount": 1,
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Detail action reference](actions/get-user-detail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kommunicate/latest/actions/get-user-detail).

## Change Conversation Assignee

Updates a conversation assignee in Kommunicate.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "assignee": "string",
  "ofUserId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/change-conversation-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "assignee": "string",
    "ofUserId": "string"
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
      "generatedAt": 1,
      "response": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Conversation Assignee action reference](actions/change-conversation-assignee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kommunicate/latest/actions/change-conversation-assignee).
