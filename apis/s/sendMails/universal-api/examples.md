# SendMails Universal API Examples

These examples use the MindCloud API key and SendMails connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Lists

Retrieves a list of lists from SendMails.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists?${params}`, {
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
      "clickRate": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "openRate": "string",
      "subscribers": "string",
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Lists action reference](actions/get-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendMails/latest/actions/get-lists).

## Add List Field

Adds a custom field to a list in SendMails.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-list-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string",
  "type": "string",
  "label": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/add-list-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string",
    "type": "string",
    "label": "string",
    "tag": "string"
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
      "field": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add List Field action reference](actions/add-list-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendMails/latest/actions/add-list-field).
