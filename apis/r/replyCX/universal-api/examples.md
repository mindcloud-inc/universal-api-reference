# ReplyCX Universal API Examples

These examples use the MindCloud API key and ReplyCX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/list-bots?${params}`, {
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
      "botLeadId": 1,
      "botOwnerId": 1,
      "botOwnerName": "Ava Chen",
      "botTitle": "string",
      "campaignDetails": {},
      "categoryName": {},
      "channels": [
        {
          "configurationId": 1,
          "name": "Ava Chen"
        }
      ],
      "createdAt": "string",
      "designTool": "string",
      "isActive": true,
      "isInactiveBySystem": true,
      "isPreferredBot": true,
      "isVisible": 1,
      "lastDeployedAt": "string",
      "outboundType": {},
      "preferredBotLanguage": {
        "code": "string",
        "label": "string"
      },
      "previewKey": "string",
      "priority": 1,
      "publishKey": "string",
      "role": {
        "id": 1,
        "role": "string"
      },
      "spreadsheetLink": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/replyCX/latest/actions/list-bots).

## Change Conversation Assignee



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/change-conversation-assignee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "user.by": "string",
  "user.to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/change-conversation-assignee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "user.by": "string",
    "user.to": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Change Conversation Assignee action reference](actions/change-conversation-assignee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/replyCX/latest/actions/change-conversation-assignee).
