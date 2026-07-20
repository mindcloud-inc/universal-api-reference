# Becon Universal API Examples

These examples use the MindCloud API key and Becon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Currencies

Retrieves available currencies and chains from Becon.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies?${params}`, {
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
      "chain": "string",
      "id": 1,
      "iso_name": "Ava Chen",
      "logo": "string",
      "name": "Ava Chen",
      "network": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Currencies action reference](actions/list-currencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/becon/latest/actions/list-currencies).

## Create Binance Address

Creates a new Binance payment address in Becon.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-binance-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "binance",
  "external_id": "string",
  "origin_amount": "string",
  "origin_currency": "string",
  "payment_currency": "BNB"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/becon/latest/actions/create-binance-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "binance",
    "external_id": "string",
    "origin_amount": "string",
    "origin_currency": "string",
    "payment_currency": "BNB"
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
      "address": "string",
      "message": "string",
      "payment_amount": "string",
      "payment_currency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Binance Address action reference](actions/create-binance-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/becon/latest/actions/create-binance-address).
