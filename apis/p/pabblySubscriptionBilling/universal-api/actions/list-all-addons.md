# Pabbly Subscription Billing: List All Addons



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-addons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-addons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-addons?${params}`, {
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
      "associatePlans": "string",
      "billingCycle": "string",
      "billingPeriod": "string",
      "categoryArray": [
        "string"
      ],
      "categoryList": [
        {}
      ],
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "plansArray": [
        "string"
      ],
      "price": 1,
      "productId": "string",
      "status": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatePlans` | string |  |
| `billingCycle` | string |  |
| `billingPeriod` | string |  |
| `categoryArray` | array<string> |  |
| `categoryList` | array<object> |  |
| `code` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `plansArray` | array<string> |  |
| `price` | number |  |
| `productId` | string |  |
| `status` | boolean |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/addons/:productId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-addons.md) for the provider-specific parameters and requirements.

