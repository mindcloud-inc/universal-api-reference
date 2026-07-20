# Beds24 Universal API Examples

These examples use the MindCloud API key and Beds24 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Details

Retrieves token details and diagnostics from Beds24.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details?${params}`, {
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
      "diagnostics": {},
      "token": {},
      "validToken": true
    }
  ],
  "meta": {}
}
```

See the full [Get Token Details action reference](actions/get-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beds24/latest/actions/get-token-details).

## Add Stripe Payment Method

Adds a Stripe payment method in Beds24.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/add-stripe-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beds24/latest/actions/add-stripe-payment-method', {
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
      "errors": [
        {}
      ],
      "info": [
        {}
      ],
      "modified": {},
      "new": {},
      "success": true,
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Stripe Payment Method action reference](actions/add-stripe-payment-method.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beds24/latest/actions/add-stripe-payment-method).
