# Reepay Universal API Examples

These examples use the MindCloud API key and Reepay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Reepay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers?${params}`, {
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
      "active_subscriptions": 1,
      "cancelled_amount": 1,
      "cancelled_invoices": 1,
      "cancelled_subscriptions": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "failed_amount": 1,
      "failed_invoices": 1,
      "handle": "string",
      "pending_amount": 1,
      "pending_invoices": 1,
      "phone": "string",
      "refunded_amount": 1,
      "settled_amount": 1,
      "settled_invoices": 1,
      "subscriptions": 1,
      "test": true
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reepay/latest/actions/list-customers).

## Add Offline Payment Method

Adds an offline payment method in Reepay.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-offline-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offline_agreement_handle": "codex-rtv-1775066629-offline"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reepay/latest/actions/add-offline-payment-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offline_agreement_handle": "codex-rtv-1775066629-offline"
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
      "created": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "id": "string",
      "offline_mandate": {
        "offline_agreement_handle": "string",
        "offline_agreement_name": "Ava Chen"
      },
      "payment_type": "string",
      "reference": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Offline Payment Method action reference](actions/add-offline-payment-method.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reepay/latest/actions/add-offline-payment-method).
