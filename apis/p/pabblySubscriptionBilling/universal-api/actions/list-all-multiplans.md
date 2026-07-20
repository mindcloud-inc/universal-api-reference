# Pabbly Subscription Billing: List All Multiplans



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-multiplans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-multiplans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-multiplans?${params}`, {
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
      "checkoutPage": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "multiplanList": "string",
      "pageTitle": "string",
      "plans": [
        {}
      ],
      "preferredPlanId": "string",
      "productId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutPage` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `multiplanList` | string |  |
| `pageTitle` | string |  |
| `plans` | array<object> |  |
| `preferredPlanId` | string |  |
| `productId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/multiplans` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-multiplans.md) for the provider-specific parameters and requirements.

