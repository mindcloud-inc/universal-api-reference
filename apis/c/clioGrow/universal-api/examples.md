# Clio Grow Universal API Examples

These examples use the MindCloud API key and Clio Grow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clioGrow/latest/actions/get-current-user).

## Create Contact Note



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-contact-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "subject": "string",
    "body": "string"
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
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact Note action reference](actions/create-contact-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clioGrow/latest/actions/create-contact-note).
