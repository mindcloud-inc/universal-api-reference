# Braintree Universal API Examples

These examples use the MindCloud API key and Braintree connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Retrieves a ping response from Braintree.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/braintree/latest/actions/ping).

## Create Client Token

Creates a new client token in Braintree.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/create-client-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/braintree/latest/actions/create-client-token', {
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
      "clientToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client Token action reference](actions/create-client-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/braintree/latest/actions/create-client-token).
