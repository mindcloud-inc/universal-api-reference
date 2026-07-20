# Eduzz Universal API Examples

These examples use the MindCloud API key and Eduzz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Profile

Retrieves the logged-in user profile from Eduzz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-account-profile?${params}`, {
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

See the full [Get Account Profile action reference](actions/get-account-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eduzz/latest/actions/get-account-profile).

## Create Checkout Cart

Creates a checkout cart in Eduzz.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/create-checkout-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/create-checkout-cart', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Checkout Cart action reference](actions/create-checkout-cart.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eduzz/latest/actions/create-checkout-cart).
