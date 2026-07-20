# Google Mail Universal API Examples

These examples use the MindCloud API key and Google Mail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Labels

Retrieves labels from a Gmail mailbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels?${params}`, {
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
      "id": "string",
      "labelListVisibility": "string",
      "messageListVisibility": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Labels action reference](actions/list-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gmail/latest/actions/list-labels).

## Batch Modify Emails

Updates labels on multiple Gmail messages.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/batch-modify-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/batch-modify-emails', {
  method: 'PUT',
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
      "addLabelIds": [
        "string"
      ],
      "ids": [
        "string"
      ],
      "removeLabelIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Batch Modify Emails action reference](actions/batch-modify-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gmail/latest/actions/batch-modify-emails).
