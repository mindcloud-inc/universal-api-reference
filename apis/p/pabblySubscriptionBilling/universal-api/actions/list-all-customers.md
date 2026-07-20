# Pabbly Subscription Billing: List All Customers



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers?${params}`, {
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
      "billingAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "stateCode": "string",
        "street1": "string",
        "zipCode": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "shippingAddress": {
        "city": "string",
        "country": "string",
        "state": "string",
        "stateCode": "string",
        "street1": "string",
        "zipCode": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.stateCode` | string |  |
| `billingAddress.street1` | string |  |
| `billingAddress.zipCode` | string |  |
| `createdAt` | date |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.state` | string |  |
| `shippingAddress.stateCode` | string |  |
| `shippingAddress.street1` | string |  |
| `shippingAddress.zipCode` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/customers` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-customers.md) for the provider-specific parameters and requirements.

