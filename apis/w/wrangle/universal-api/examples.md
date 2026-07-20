# Wrangle Universal API Examples

These examples use the MindCloud API key and Wrangle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Inboxes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/get-inboxes?${params}`, {
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
      "inboxes": [
        {
          "createdAt": "string",
          "creatorId": "string",
          "defaultUserRole": "string",
          "description": {},
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "updatedAt": "string",
          "userRoles": [
            {
              "role": "string",
              "userId": "string"
            }
          ]
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Inboxes action reference](actions/get-inboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wrangle/latest/actions/get-inboxes).

## Create Ticket



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Quarterly access request",
  "inboxId": "inbox_uuid",
  "requesterId": "U12345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Quarterly access request",
    "inboxId": "inbox_uuid",
    "requesterId": "U12345678"
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
      "success": true,
      "ticket": {
        "assigneeId": {},
        "createdAt": "string",
        "creatorId": "string",
        "csatReason": {},
        "csatScore": {},
        "description": "string",
        "id": "string",
        "inboxId": "string",
        "name": "Ava Chen",
        "priority": "string",
        "requesterId": "string",
        "slackMessageChannel": "string",
        "slackMessageTs": "string",
        "slackOriginalMessage": {},
        "slackParentMessageTs": "string",
        "slackPermalinkUrl": "https://example.com",
        "status": "string",
        "updatedAt": "string",
        "workspaceId": "string",
        "workspaceTicketNumber": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Ticket action reference](actions/create-ticket.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wrangle/latest/actions/create-ticket).
