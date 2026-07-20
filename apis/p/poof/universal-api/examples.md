# Poof Universal API Examples

These examples use the MindCloud API key and Poof connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Price

Retrieves a price quote from Poof.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price?connectionId=$CONNECTION_ID&crypto=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crypto": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-price?${params}`, {
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

See the full [Fetch Price action reference](actions/fetch-price.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/poof/latest/actions/fetch-price).

## Create Wallet

Creates a new wallet in Poof.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-a-wallet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": "polygon"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-a-wallet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": "polygon"
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

See the full [Create Wallet action reference](actions/create-a-wallet.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/poof/latest/actions/create-a-wallet).
