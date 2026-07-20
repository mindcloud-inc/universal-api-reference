# Raklet: List Payments



```
GET https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/list-payments?${params}`, {
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
      "amount": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": 1,
      "id": "string",
      "isManualPayment": true,
      "isRecurringPayment": true,
      "memberName": "Ava Chen",
      "organisationMembershipId": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": 1,
      "referenceNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdOn` | date |  |
| `currency` | number |  |
| `id` | string |  |
| `isManualPayment` | boolean |  |
| `isRecurringPayment` | boolean |  |
| `memberName` | string |  |
| `organisationMembershipId` | string |  |
| `paymentDate` | date |  |
| `paymentMethod` | number |  |
| `referenceNumber` | string |  |

## Native endpoint

Through the native Raklet API, this operation is `GET /organisations/:organisationId/payments` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

