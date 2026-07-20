# OPN Universal API Examples

These examples use the MindCloud API key and OPN connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves account balance details from OPN.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-balance?${params}`, {
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
      "at": "string",
      "created_at": "string",
      "currency": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "on_hold": 1,
      "reserve": 1,
      "total": 1,
      "transferable": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oPN/latest/actions/get-balance).

## Accept Dispute

Accepts an existing dispute in OPN.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/accept-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/accept-dispute', {
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
      "admin_message": "string",
      "amount": 1,
      "charge": "string",
      "closed_at": "string",
      "created_at": "string",
      "currency": "string",
      "documents": {},
      "funding_amount": 1,
      "funding_currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "message": "string",
      "metadata": {},
      "object": "string",
      "reason_code": "string",
      "reason_message": "string",
      "status": "string",
      "transactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Accept Dispute action reference](actions/accept-dispute.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oPN/latest/actions/accept-dispute).
