# Razorpay: List Payment Links

Retrieves payment link records from Razorpay.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-payment-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-payment-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-payment-links?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentLinks": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentLinks[]` | array<object> |  |
| `paymentLinks[].acceptPartial` | boolean |  |
| `paymentLinks[].amount` | number |  |
| `paymentLinks[].amountPaid` | number |  |
| `paymentLinks[].cancelledAt` | number |  |
| `paymentLinks[].createdAt` | number |  |
| `paymentLinks[].currency` | string |  |
| `paymentLinks[].customer[]` | array<string> |  |
| `paymentLinks[].description` | string |  |
| `paymentLinks[].expireBy` | number |  |
| `paymentLinks[].expiredAt` | number |  |
| `paymentLinks[].firstMinPartialAmount` | number |  |
| `paymentLinks[].id` | string |  |
| `paymentLinks[].notes[]` | array<string> |  |
| `paymentLinks[].notify` | object |  |
| `paymentLinks[].notify.email` | boolean |  |
| `paymentLinks[].notify.sms` | boolean |  |
| `paymentLinks[].notify.whatsapp` | boolean |  |
| `paymentLinks[].payments` | object |  |
| `paymentLinks[].referenceId` | string |  |
| `paymentLinks[].reminderEnable` | boolean |  |
| `paymentLinks[].reminders[]` | array<string> |  |
| `paymentLinks[].shortUrl` | string |  |
| `paymentLinks[].status` | string |  |
| `paymentLinks[].updatedAt` | number |  |
| `paymentLinks[].upiLink` | boolean |  |
| `paymentLinks[].userId` | string |  |
| `paymentLinks[].whatsappLink` | boolean |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/payment_links/` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-links.md) for the provider-specific parameters and requirements.

