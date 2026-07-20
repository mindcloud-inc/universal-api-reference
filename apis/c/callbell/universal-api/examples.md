# Callbell Universal API Examples

These examples use the MindCloud API key and Callbell connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Auth Me

Retrieves current authenticated user details from Callbell.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-auth-me?${params}`, {
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
      "api_key": "string",
      "status": "string",
      "user_email": "ava@example.com",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Me action reference](actions/get-auth-me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callbell/latest/actions/get-auth-me).

## Close Contact Conversation

Closes a contact conversation in Callbell.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/close-contact-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callbell/latest/actions/close-contact-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
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
      "assignedUser": {},
      "avatarUrl": "https://example.com",
      "blockedAt": "string",
      "channel": {},
      "closedAt": "string",
      "conversationHref": "string",
      "createdAt": "string",
      "customFields": {},
      "funnelId": "string",
      "href": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "source": "string",
      "tags": [
        "string"
      ],
      "team": {},
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Contact Conversation action reference](actions/close-contact-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callbell/latest/actions/close-contact-conversation).
