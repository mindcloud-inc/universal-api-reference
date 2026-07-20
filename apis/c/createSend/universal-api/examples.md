# CreateSend Universal API Examples

These examples use the MindCloud API key and CreateSend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients

Retrieves clients from CreateSend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-clients?${params}`, {
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
      "ClientID": "string",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/createSend/latest/actions/list-clients).

## Add Subscriber

Creates a new subscriber in CreateSend.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "c9026d1f12bd6b3e41844e3257f4d603",
  "emailAddress": "codex-stage4-default@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/createSend/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "c9026d1f12bd6b3e41844e3257f4d603",
    "emailAddress": "codex-stage4-default@example.com"
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
      "emailAddress": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Subscriber action reference](actions/add-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/createSend/latest/actions/add-subscriber).
