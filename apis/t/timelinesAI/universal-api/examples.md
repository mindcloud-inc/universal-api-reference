# TimelinesAI Universal API Examples

These examples use the MindCloud API key and TimelinesAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List WhatsApp Accounts

Retrieves WhatsApp accounts connected in TimelinesAI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts?${params}`, {
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
      "data": {
        "whatsappAccounts": [
          {
            "accountName": "Ava Chen",
            "connectedOn": "string",
            "id": "string",
            "ownerEmail": "ava@example.com",
            "ownerName": "Ava Chen",
            "phone": "string",
            "status": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List WhatsApp Accounts action reference](actions/list-whatsapp-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timelinesAI/latest/actions/list-whatsapp-accounts).

## Add Chat Labels

Adds labels to a specific TimelinesAI chat.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/add-chat-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": 1,
  "labels[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/add-chat-labels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": 1,
    "labels[]": ["string"]
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
      "data": {
        "labels": [
          "string"
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Chat Labels action reference](actions/add-chat-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timelinesAI/latest/actions/add-chat-labels).
