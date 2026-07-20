# TrueLayer Universal API Examples

These examples use the MindCloud API key and TrueLayer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Merchant Accounts

Retrieves merchant accounts from TrueLayer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/list-merchant-accounts?${params}`, {
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
      "account_identifiers": [
        {}
      ],
      "available_balance": 1,
      "currency": "string",
      "current_balance": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Merchant Accounts action reference](actions/list-merchant-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trueLayer/latest/actions/list-merchant-accounts).

## Cancel Payment

Cancels a payment in TrueLayer.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/cancel-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/cancel-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "cancelled_at": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Payment action reference](actions/cancel-payment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trueLayer/latest/actions/cancel-payment).
