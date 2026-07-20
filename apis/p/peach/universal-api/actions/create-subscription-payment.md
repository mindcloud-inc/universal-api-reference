# Peach: Create Subscription Payment

Creates a subscription payment in Peach.

```
POST https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-subscription-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-subscription-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sum": 1,
  "billingCycles": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-subscription-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sum": 1,
    "billingCycles": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sum` | number | yes | Payment sum. |
| `billingCycles` | number | yes | Total number of billing cycles. |
| `firstName` | string | no | Donor first name. |
| `lastName` | string | no | Donor last name. |
| `email` | string | no | Donor email address. |
| `phone` | string | no | Donor phone number. |
| `displayName` | string | no | Display name for the donor. |
| `currency` | string | no | Donation currency. Peach defaults to ILS. |
| `campaignId` | string | no | Campaign ID for the payment. |
| `groupId` | string | no | Group ID for the payment. |
| `contactId` | string | no | Existing Peach contact ID for the donor. |
| `customProperties` | object | no | Custom properties for the payment. |
| `triggerAutomations` | boolean | no | Set to true only if the payment should trigger automations in Peach. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "campaignId": "string",
      "cancelled": true,
      "completed": true,
      "contactId": "string",
      "createdAt": 1,
      "customProperties": {},
      "donationCurrency": "string",
      "donationSum": 1,
      "donorDisplayName": "Ava Chen",
      "email": "ava@example.com",
      "expectedHokEndDate": "2026-05-07T12:00:00.000Z",
      "items": [
        {}
      ],
      "paymentDate": 1,
      "paymentId": "string",
      "paymentType": "string",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `campaignId` | string |  |
| `cancelled` | boolean |  |
| `completed` | boolean |  |
| `contactId` | string |  |
| `createdAt` | number |  |
| `customProperties` | object |  |
| `donationCurrency` | string |  |
| `donationSum` | number |  |
| `donorDisplayName` | string |  |
| `email` | string |  |
| `expectedHokEndDate` | date |  |
| `items` | array<object> |  |
| `paymentDate` | number |  |
| `paymentId` | string |  |
| `paymentType` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Peach API, this operation is `POST /payments` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription-payment.md) for the provider-specific parameters and requirements.

