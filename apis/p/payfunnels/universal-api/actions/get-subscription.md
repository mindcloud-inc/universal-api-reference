# Payfunnels: Get Subscription

Retrieves a subscription from Payfunnels by ID.

```
GET https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-subscription?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-subscription?${params}`, {
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
| `id` | string | yes | The ID of the subscription to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "chargeAmount": 1,
      "createdAt": "string",
      "customer": {},
      "endDate": "string",
      "id": "string",
      "metadata": {},
      "paymentMethod": {},
      "paymentType": "string",
      "startDate": "string",
      "status": "string",
      "title": "string",
      "totalCollectedAmount": 1,
      "totalDueAmount": 1,
      "totalMaxPayment": 1,
      "totalSubscriptionAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `chargeAmount` | number |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `endDate` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `paymentMethod` | object |  |
| `paymentType` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `title` | string |  |
| `totalCollectedAmount` | number |  |
| `totalDueAmount` | number |  |
| `totalMaxPayment` | number |  |
| `totalSubscriptionAmount` | number |  |

## Native endpoint

Through the native Payfunnels API, this operation is `GET /v1/subscriptions/{id}` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

