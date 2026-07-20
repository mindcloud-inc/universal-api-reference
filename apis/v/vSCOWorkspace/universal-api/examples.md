# VSCO Workspace Universal API Examples

These examples use the MindCloud API key and VSCO Workspace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Studio

Retrieves your studio details from VSCO Workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio?${params}`, {
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
      "cacheVersion": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "dateFormat": "string",
      "decimalSeparator": "string",
      "defaultBrandId": "string",
      "email": "ava@example.com",
      "externalMappings": [
        {}
      ],
      "hidden": true,
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": {},
      "readonlyEnabled": true,
      "readonlyEnabledAt": {},
      "temperature": "string",
      "thousandsSeparator": "string",
      "timeFormat": "string",
      "timezoneId": "string",
      "weekStartsOn": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My Studio action reference](actions/get-my-studio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vSCOWorkspace/latest/actions/get-my-studio).

## Apply Payment to Order

Applies a payment to an order in VSCO Workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/apply-payment-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "orderId": "string",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/apply-payment-to-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "orderId": "string",
    "amount": 1
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
      "authCode": "string",
      "checkNumber": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "id": "string",
      "invoiceItemId": "string",
      "jobId": "string",
      "memo": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "payerId": "string",
      "paymentAllocations": [
        {}
      ],
      "paymentMethodId": "string",
      "processedViaClientAccess": true,
      "received": "2026-05-07T12:00:00.000Z",
      "refundedAmount": {},
      "refunds": [
        {}
      ],
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Apply Payment to Order action reference](actions/apply-payment-to-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vSCOWorkspace/latest/actions/apply-payment-to-order).
