# iPaymu Universal API Examples

These examples use the MindCloud API key and iPaymu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Balance

Check your iPaymu account balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance?${params}`, {
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
      "memberBalance": 1,
      "merchantBalance": 1,
      "va": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Balance action reference](actions/check-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPaymu/latest/actions/check-balance).

## Create Direct Payment

Create a direct payment and return the payment details for the selected channel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-direct-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string",
  "email": "ava@example.com",
  "amount": 1,
  "notifyUrl": "https://example.com",
  "referenceId": "string",
  "paymentMethod": "string",
  "paymentChannel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-direct-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string",
    "email": "ava@example.com",
    "amount": 1,
    "notifyUrl": "https://example.com",
    "referenceId": "string",
    "paymentMethod": "string",
    "paymentChannel": "string"
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
      "channel": "string",
      "escrow": true,
      "expired": "string",
      "fee": 1,
      "feeDirection": "string",
      "paymentName": "Ava Chen",
      "paymentNo": "string",
      "referenceId": "string",
      "sessionId": "string",
      "subTotal": 1,
      "total": 1,
      "transactionId": 1,
      "via": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Direct Payment action reference](actions/create-direct-payment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/iPaymu/latest/actions/create-direct-payment).
