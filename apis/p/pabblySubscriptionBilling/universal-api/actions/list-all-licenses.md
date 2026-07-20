# Pabbly Subscription Billing: List All Licenses



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-licenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-licenses?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "licenseCodes": [
        {}
      ],
      "method": "string",
      "name": "Ava Chen",
      "planId": "string",
      "status": "string",
      "totalLicense": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usedLicense": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `licenseCodes` | array<object> |  |
| `method` | string |  |
| `name` | string |  |
| `planId` | string |  |
| `status` | string |  |
| `totalLicense` | number |  |
| `updatedAt` | date |  |
| `usedLicense` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/products/:productId/licenses` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-licenses.md) for the provider-specific parameters and requirements.

