# Chatwork Universal API Examples

These examples use the MindCloud API key and Chatwork connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/get-my-profile?${params}`, {
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
      "accountId": 1,
      "avatarImageUrl": "https://example.com",
      "chatworkId": "string",
      "department": "string",
      "facebook": "string",
      "introduction": "string",
      "loginMail": "string",
      "mail": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "roomId": 1,
      "skype": "string",
      "telExtension": "string",
      "telMobile": "string",
      "telOrganization": "string",
      "title": "string",
      "twitter": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatwork/latest/actions/get-my-profile).

## Create Chat Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-chat-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "123456789",
  "body": "Buy milk",
  "toIds": "1,3,6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatwork/latest/actions/create-chat-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "123456789",
    "body": "Buy milk",
    "toIds": "1,3,6"
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
      "taskIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Chat Task action reference](actions/create-chat-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatwork/latest/actions/create-chat-task).
