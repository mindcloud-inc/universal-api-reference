# BlueSnap Universal API Examples

These examples use the MindCloud API key and BlueSnap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Plans

Retrieves plans from BlueSnap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-plans?${params}`, {
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
      "lastPage": true,
      "plans": [
        {
          "chargeFrequency": "string",
          "currency": "string",
          "name": "Ava Chen",
          "planId": 1,
          "recurringChargeAmount": 1,
          "status": "string"
        }
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

See the full [List Plans action reference](actions/list-plans.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueSnap/latest/actions/list-plans).

## Capture Authorized Transaction

Captures an authorized BlueSnap transaction.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/capture-authorized-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string",
  "amount": "string",
  "currency": "string",
  "cardTransactionType": "CAPTURE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/capture-authorized-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "string",
    "amount": "string",
    "currency": "string",
    "cardTransactionType": "CAPTURE"
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
      "amount": 1,
      "cardTransactionType": "string",
      "currency": "string",
      "openToCapture": 1,
      "processingInfo": {
        "processingStatus": "string"
      },
      "transactionId": "string",
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

See the full [Capture Authorized Transaction action reference](actions/capture-authorized-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/blueSnap/latest/actions/capture-authorized-transaction).
