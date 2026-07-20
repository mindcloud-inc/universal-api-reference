# Razorpay: Update Payment Link

Updates an existing payment link in Razorpay.

```
PUT https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-payment-link', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the payment link. |
| `acceptPartial` | boolean | no |  |
| `referenceId` | string | no |  |
| `expireBy` | number | no |  |
| `notes` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptPartial": true,
      "amount": 1,
      "amountPaid": 1,
      "cancelledAt": 1,
      "createdAt": 1,
      "currency": "string",
      "customer": [
        [
          "string"
        ]
      ],
      "description": "string",
      "expireBy": 1,
      "expiredAt": 1,
      "firstMinPartialAmount": 1,
      "id": "string",
      "notes": {},
      "notify": {
        "email": true,
        "sms": true,
        "whatsapp": true
      },
      "payments": [
        [
          "string"
        ]
      ],
      "referenceId": "string",
      "reminderEnable": true,
      "reminders": {
        "status": "string"
      },
      "shortUrl": "https://example.com",
      "status": "string",
      "updatedAt": 1,
      "upiLink": true,
      "userId": "string",
      "whatsappLink": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptPartial` | boolean |  |
| `amount` | number |  |
| `amountPaid` | number |  |
| `cancelledAt` | number |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `customer[]` | array<string> |  |
| `description` | string |  |
| `expireBy` | number |  |
| `expiredAt` | number |  |
| `firstMinPartialAmount` | number |  |
| `id` | string |  |
| `notes` | object |  |
| `notify` | object |  |
| `notify.email` | boolean |  |
| `notify.sms` | boolean |  |
| `notify.whatsapp` | boolean |  |
| `payments[]` | array<string> |  |
| `referenceId` | string |  |
| `reminderEnable` | boolean |  |
| `reminders` | object |  |
| `reminders.status` | string |  |
| `shortUrl` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |
| `upiLink` | boolean |  |
| `userId` | string |  |
| `whatsappLink` | boolean |  |

## Native endpoint

Through the native Razorpay API, this operation is `PATCH /v1/payment_links/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-link.md) for the provider-specific parameters and requirements.

