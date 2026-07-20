# Sendcrux Universal API Examples

These examples use the MindCloud API key and Sendcrux connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Email Lists

Retrieves a list of email lists from Sendcrux.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-email-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-email-lists?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {},
      "permissions": {}
    }
  ],
  "meta": {}
}
```

See the full [List Email Lists action reference](actions/list-email-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendcrux/latest/actions/list-email-lists).

## Add Email List Field

Creates a custom field for an email list in Sendcrux.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/add-email-list-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "tag": "string",
  "type": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/add-email-list-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "tag": "string",
    "type": "string",
    "uid": "string"
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

See the full [Add Email List Field action reference](actions/add-email-list-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendcrux/latest/actions/add-email-list-field).
