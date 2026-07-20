# OneDeck Universal API Examples

These examples use the MindCloud API key and OneDeck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from OneDeck.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users?${params}`, {
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
      "createDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "image": {},
      "isLanguageRtl": {},
      "lastName": "Chen",
      "role": "string",
      "status": "string",
      "twoFaEnabled": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": {}
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneDeck/latest/actions/list-users).

## Create Record

Creates a new record in a OneDeck board.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
  "name": "MindCloud Test Record"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
    "name": "MindCloud Test Record"
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

See the full [Create Record action reference](actions/create-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneDeck/latest/actions/create-record).
