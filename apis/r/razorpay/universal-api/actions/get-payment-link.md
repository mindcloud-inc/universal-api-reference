# Razorpay: Get Payment Link

Retrieves a payment link from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment-link?${params}`, {
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
| `id` | string | yes | Unique identifier of the payment link. |

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

Through the native Razorpay API, this operation is `GET /v1/payment_links/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-link.md) for the provider-specific parameters and requirements.

