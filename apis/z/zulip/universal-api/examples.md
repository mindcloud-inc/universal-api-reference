# Zulip Universal API Examples

These examples use the MindCloud API key and Zulip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Own User

Retrieves the requesting user's Zulip account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "avatar_version": 1,
      "bot_owner_id": 1,
      "bot_type": 1,
      "date_joined": "string",
      "delivery_email": "ava@example.com",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "is_active": true,
      "is_admin": true,
      "is_bot": true,
      "is_guest": true,
      "is_imported_stub": true,
      "is_owner": true,
      "max_message_id": 1,
      "msg": "string",
      "result": "string",
      "role": 1,
      "timezone": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Own User action reference](actions/get-own-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zulip/latest/actions/get-own-user).

## Add Emoji Reaction

Adds an emoji reaction to a Zulip message.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/add-emoji-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emojiName": "Ava Chen",
  "messageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zulip/latest/actions/add-emoji-reaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emojiName": "Ava Chen",
    "messageId": 1
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
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Emoji Reaction action reference](actions/add-emoji-reaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zulip/latest/actions/add-emoji-reaction).
