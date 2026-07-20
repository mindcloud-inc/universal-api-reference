# ChargeBee Universal API Examples

These examples use the MindCloud API key and ChargeBee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Events



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events?${params}`, {
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
      "api_version": "string",
      "content": {},
      "event_type": "string",
      "id": "string",
      "object": "string",
      "occurred_at": 1,
      "source": "string",
      "webhook_status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Events action reference](actions/list-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeBee/latest/actions/list-events).

## Create Customer

Creates a new customer in ChargeBee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/create-customer', {
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
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "object": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chargeBee/latest/actions/create-customer).
