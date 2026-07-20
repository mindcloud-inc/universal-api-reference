# Umbler Talk Universal API Examples

These examples use the MindCloud API key and Umbler Talk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Member

Retrieves the current member profile from Umbler Talk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-current-member?${params}`, {
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
      "_t": "string",
      "cellphone": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "id": "string",
      "organizations": [
        {}
      ],
      "profilePictureUrl": "https://example.com",
      "signature": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Member action reference](actions/get-current-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umblerTalk/latest/actions/get-current-member).

## Create Chat

Finds a chat in Umbler Talk, or creates one if needed.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "contactId": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "contactId": "string",
    "organizationId": "string"
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
      "_t": "string",
      "channel": {},
      "contact": {},
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "hasMessagesBeforeAllowedHistory": true,
      "id": "string",
      "lastMessage": {},
      "latestMessages": [
        {}
      ],
      "open": true,
      "organization": {},
      "private": true,
      "sector": {},
      "tags": [
        {}
      ],
      "waiting": true
    }
  ],
  "meta": {}
}
```

See the full [Create Chat action reference](actions/create-chat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umblerTalk/latest/actions/create-chat).
