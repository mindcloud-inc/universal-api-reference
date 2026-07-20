# Missive Universal API Examples

These examples use the MindCloud API key and Missive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Conversation

Retrieves a conversation from your Missive workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation?${params}`, {
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
      "appUrl": "https://example.com",
      "assigneeEmails": "ava@example.com",
      "assigneeNames": "Ava Chen",
      "attachmentsCount": 1,
      "closedAt": {},
      "color": {},
      "completedTasksCount": 1,
      "createdAt": 1,
      "draftsCount": 1,
      "id": "string",
      "lastActivityAt": 1,
      "latestMessageSubject": {},
      "messagesCount": 1,
      "organization": {},
      "sendLaterMessagesCount": 1,
      "sharedLabelNames": "Ava Chen",
      "subject": {},
      "tasksCount": 1,
      "team": {},
      "users": [
        {
          "archived": true,
          "assigned": true,
          "closed": true,
          "email": "ava@example.com",
          "flagged": true,
          "id": "string",
          "junked": true,
          "name": "Ava Chen",
          "snoozed": true,
          "trashed": true,
          "unassigned": true
        }
      ],
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Conversation action reference](actions/get-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/missive/latest/actions/get-conversation).

## Create Draft

Creates a draft in your Missive workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "conversation": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Draft action reference](actions/create-draft.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/missive/latest/actions/create-draft).
