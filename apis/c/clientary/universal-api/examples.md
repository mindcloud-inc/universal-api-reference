# Clientary Universal API Examples

These examples use the MindCloud API key and Clientary connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients

Retrieves clients from your Clientary account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-clients?${params}`, {
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
      "account": {
        "currencyCode": "string"
      },
      "address": "string",
      "amountOutstanding": 1,
      "city": "string",
      "contactViewable": true,
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "notesCount": 1,
      "number": "string",
      "pendingInvoices": 1,
      "state": "string",
      "status": "string",
      "unbilledProjectsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usersCount": 1,
      "wasLead": true,
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clientary/latest/actions/list-clients).

## Create Client

Creates a new client in Clientary.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client.name": "Ava Chen"
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
      "account": {
        "currencyCode": "string"
      },
      "address": "string",
      "amountOutstanding": 1,
      "city": "string",
      "contactViewable": true,
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "notesCount": 1,
      "number": "string",
      "pendingInvoices": 1,
      "state": "string",
      "status": "string",
      "unbilledProjectsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usersCount": 1,
      "wasLead": true,
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clientary/latest/actions/create-client).
