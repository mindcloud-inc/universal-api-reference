# Parsio Universal API Examples

These examples use the MindCloud API key and Parsio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mailboxes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes?${params}`, {
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
      "collectEmails": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailPrefix": "ava@example.com",
      "isActive": true,
      "name": "Ava Chen",
      "processAttachments": true,
      "stats": {
        "docsFailed": 1,
        "docsParsed": 1,
        "docsTotal": 1
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Mailboxes action reference](actions/list-mailboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parsio/latest/actions/list-mailboxes).

## Create HTML or Text Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/create-html-or-text-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parsio/latest/actions/create-html-or-text-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": "string",
    "name": "Ava Chen"
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

See the full [Create HTML or Text Document action reference](actions/create-html-or-text-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/parsio/latest/actions/create-html-or-text-document).
