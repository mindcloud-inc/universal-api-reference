# Razorpay Universal API Examples

These examples use the MindCloud API key and Razorpay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dispute

Retrieves a dispute from Razorpay by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-dispute?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-dispute?${params}`, {
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
      "accessActivityLog": [
        "string"
      ],
      "amount": 1,
      "amountDeducted": 1,
      "billingProof": [
        "string"
      ],
      "cancellationProof": [
        "string"
      ],
      "createdAt": 1,
      "currency": "string",
      "customerCommunication": [
        "string"
      ],
      "documentIds": [
        "string"
      ],
      "entity": "string",
      "explanationLetter": [
        "string"
      ],
      "id": "string",
      "paymentId": "string",
      "phase": "string",
      "proofOfService": [
        "string"
      ],
      "reasonCode": "string",
      "reasonDescription": "string",
      "refundCancellationPolicy": [
        "string"
      ],
      "refundConfirmation": [
        "string"
      ],
      "respondBy": 1,
      "shippingProof": [
        "string"
      ],
      "status": "string",
      "submittedAt": 1,
      "summary": "string",
      "termAndConditions": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Dispute action reference](actions/get-dispute.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/razorpay/latest/actions/get-dispute).

## Accept Dispute

Accepts a dispute in Razorpay as lost.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/accept-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/accept-dispute', {
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
      "accessActivityLog": [
        "string"
      ],
      "amount": 1,
      "amountDeducted": 1,
      "billingProof": [
        "string"
      ],
      "cancellationProof": [
        "string"
      ],
      "createdAt": 1,
      "currency": "string",
      "customerCommunication": [
        "string"
      ],
      "documentIds": [
        "string"
      ],
      "entity": "string",
      "explanationLetter": [
        "string"
      ],
      "id": "string",
      "paymentId": "string",
      "phase": "string",
      "proofOfService": [
        "string"
      ],
      "reasonCode": "string",
      "reasonDescription": "string",
      "refundCancellationPolicy": [
        "string"
      ],
      "refundConfirmation": [
        "string"
      ],
      "respondBy": 1,
      "shippingProof": [
        "string"
      ],
      "status": "string",
      "submittedAt": 1,
      "summary": "string",
      "termAndConditions": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept Dispute action reference](actions/accept-dispute.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/razorpay/latest/actions/accept-dispute).
