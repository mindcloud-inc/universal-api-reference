# Payfunnels: List Subscriptions

Retrieves a list of subscriptions from Payfunnels.

```
GET https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-subscriptions?${params}`, {
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

Through the native Payfunnels API, this operation is `GET /v1/subscriptions` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

