# CloudContactAI Universal API Examples

These examples use the MindCloud API key and CloudContactAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-contacts?${params}`, {
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
      "blockIncomingSMS": true,
      "clientExternalId": "string",
      "clientId": 1,
      "collectionInfo": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "enableBotResponse": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "notes": "string",
      "originalPhone": "string",
      "pending": 1,
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userClientId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudContactAI/latest/actions/list-contacts).

## Batch Create Contacts



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/batch-create-contacts', {
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
      "clientId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Batch Create Contacts action reference](actions/batch-create-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudContactAI/latest/actions/batch-create-contacts).
