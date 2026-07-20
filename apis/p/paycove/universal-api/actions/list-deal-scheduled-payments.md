# Paycove: List Deal Scheduled Payments

Retrieves scheduled payments for a Paycove deal.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deal-scheduled-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deal-scheduled-payments?connectionId=$CONNECTION_ID&dealId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-deal-scheduled-payments?${params}`, {
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
| `dealId` | string | yes | Paycove deal id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "autoCharge": 1,
      "chargeId": {},
      "contact": {},
      "contactId": {},
      "createdAt": "string",
      "dealId": 1,
      "dealTemplate": {
        "id": {},
        "name": {}
      },
      "description": "string",
      "due": "string",
      "hasDetails": 1,
      "id": 1,
      "isPaid": 1,
      "manualPaymentNotes": {},
      "manualPaymentType": {},
      "number": 1,
      "paidAt": {},
      "paidAtDate": {},
      "payable": 1,
      "reminder": {},
      "sent": 1,
      "updatedAt": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `autoCharge` | number |  |
| `chargeId` | object |  |
| `contact` | object |  |
| `contactId` | object |  |
| `createdAt` | string |  |
| `dealId` | number |  |
| `dealTemplate.id` | object |  |
| `dealTemplate.name` | object |  |
| `description` | string |  |
| `due` | string |  |
| `hasDetails` | number |  |
| `id` | number |  |
| `isPaid` | number |  |
| `manualPaymentNotes` | object |  |
| `manualPaymentType` | object |  |
| `number` | number |  |
| `paidAt` | object |  |
| `paidAtDate` | object |  |
| `payable` | number |  |
| `reminder` | object |  |
| `sent` | number |  |
| `updatedAt` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `GET scheduled-payments/:deal_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-scheduled-payments.md) for the provider-specific parameters and requirements.

