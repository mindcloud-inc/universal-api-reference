# Razorpay: Get Dispute

Retrieves a dispute from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-dispute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the dispute. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessActivityLog` | array<string> |  |
| `amount` | number |  |
| `amountDeducted` | number |  |
| `billingProof` | array<string> |  |
| `cancellationProof` | array<string> |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `customerCommunication` | array<string> |  |
| `documentIds` | array<string> |  |
| `entity` | string |  |
| `explanationLetter` | array<string> |  |
| `id` | string |  |
| `paymentId` | string |  |
| `phase` | string |  |
| `proofOfService` | array<string> |  |
| `reasonCode` | string |  |
| `reasonDescription` | string |  |
| `refundCancellationPolicy` | array<string> |  |
| `refundConfirmation` | array<string> |  |
| `respondBy` | number |  |
| `shippingProof` | array<string> |  |
| `status` | string |  |
| `submittedAt` | number |  |
| `summary` | string |  |
| `termAndConditions` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/disputes/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dispute.md) for the provider-specific parameters and requirements.

