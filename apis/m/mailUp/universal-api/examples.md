# MailUp Universal API Examples

These examples use the MindCloud API key and MailUp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves existing mailing lists from MailUp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-lists?${params}`, {
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
      "company": "string",
      "description": "string",
      "idList": 1,
      "listGuid": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailUp/latest/actions/list-lists).

## Create Email

Creates a new email message in MailUp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idList": 1,
  "subject": "string",
  "content": "string",
  "trackingInfo": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idList": 1,
    "subject": "string",
    "content": "string",
    "trackingInfo": "[object Object]"
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
      "CreationDate": "string",
      "idList": 1,
      "idMessage": 1,
      "Notes": "string",
      "Subject": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Email action reference](actions/create-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailUp/latest/actions/create-email).
