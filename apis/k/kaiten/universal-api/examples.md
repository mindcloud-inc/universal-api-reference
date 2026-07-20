# Kaiten Universal API Examples

These examples use the MindCloud API key and Kaiten connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Current User

Retrieves the current user from Kaiten.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-current-user?${params}`, {
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
      "activated": true,
      "avatar_initials_url": "https://example.com",
      "avatar_uploaded_url": "https://example.com",
      "company_id": 1,
      "default_space_id": 1,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "last_request_date": "2026-05-07T12:00:00.000Z",
      "permissions": 1,
      "role": 1,
      "uid": "string",
      "user_id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Current User action reference](actions/retrieve-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kaiten/latest/actions/retrieve-current-user).

## Add Comment

Creates a comment on a Kaiten card.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1,
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
      "author_id": 1,
      "card_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "edited": true,
      "email_addresses_to": "ava@example.com",
      "id": 1,
      "internal": true,
      "notification_sent": true,
      "sd_description": true,
      "sd_external_recipients_cc": "string",
      "text": "string",
      "type": 1,
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kaiten/latest/actions/add-comment).
