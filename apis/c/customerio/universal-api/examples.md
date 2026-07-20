# Customer.io Universal API Examples

These examples use the MindCloud API key and Customer.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from Customer.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces?${params}`, {
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
      "billableMessagesSent": 1,
      "id": 1,
      "messagesSent": 1,
      "name": "Ava Chen",
      "objects": 1,
      "objectTypes": 1,
      "people": 1
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerio/latest/actions/list-workspaces).

## Send Transactional Email

Sends a transactional email from Customer.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionalMessageId": "password-reset",
  "identifiers": {},
  "to": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionalMessageId": "password-reset",
    "identifiers": {},
    "to": "user@example.com"
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
      "deliveryId": "string",
      "queuedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Transactional Email action reference](actions/send-transactional-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customerio/latest/actions/send-transactional-email).
