# Razorpay: Create Payment Link

Creates a new payment link in Razorpay.

```
POST https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Payment link amount in the smallest currency subunit. |
| `currency` | string | no | ISO currency code (for example INR). |
| `acceptPartial` | boolean | no |  |
| `firstMinPartialAmount` | number | no |  |
| `upiLink` | boolean | no |  |
| `description` | string | no |  |
| `referenceId` | string | no |  |
| `customer` | object | no |  |
| `notify` | object | no |  |
| `expireBy` | number | no |  |
| `notes` | object | no |  |
| `callbackUrl` | string | no |  |
| `callbackMethod` | string | no |  |
| `reminderEnable` | boolean | no |  |

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
      "payments": {},
      "referenceId": "string",
      "reminderEnable": true,
      "reminders": [
        [
          "string"
        ]
      ],
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
| `payments` | object |  |
| `referenceId` | string |  |
| `reminderEnable` | boolean |  |
| `reminders[]` | array<string> |  |
| `shortUrl` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |
| `upiLink` | boolean |  |
| `userId` | string |  |
| `whatsappLink` | boolean |  |

## Native endpoint

Through the native Razorpay API, this operation is `POST /v1/payment_links` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-link.md) for the provider-specific parameters and requirements.

