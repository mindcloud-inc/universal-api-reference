# Thinkific: Get Order

Retrieves an order record from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-order?${params}`, {
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
| `id` | number | yes | Order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateReferralCode": "string",
      "amountCents": 1,
      "amountDollars": "string",
      "couponCode": "string",
      "couponId": 1,
      "createdAt": "string",
      "id": 1,
      "items": [
        {}
      ],
      "productId": 1,
      "productName": "Ava Chen",
      "status": "string",
      "subscription": true,
      "userEmail": "ava@example.com",
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateReferralCode` | string |  |
| `amountCents` | number |  |
| `amountDollars` | string |  |
| `couponCode` | string |  |
| `couponId` | number |  |
| `createdAt` | string |  |
| `id` | number |  |
| `items` | array<object> |  |
| `productId` | number |  |
| `productName` | string |  |
| `status` | string |  |
| `subscription` | boolean |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Thinkific API, this operation is `GET /orders/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

