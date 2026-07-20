# Whop: List Payments

Retrieves payments from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-payments?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-payments?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list payments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardBrand": "string",
      "cardLast4": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": "string",
      "paidAt": "2026-05-07T12:00:00.000Z",
      "paymentMethodType": "string",
      "product": {
        "id": "string",
        "title": "string"
      },
      "refundable": true,
      "retryable": true,
      "status": "string",
      "substatus": "string",
      "total": 1,
      "user": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "voidable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardBrand` | string |  |
| `cardLast4` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `id` | string |  |
| `paidAt` | date |  |
| `paymentMethodType` | string |  |
| `product` | object |  |
| `product.id` | string |  |
| `product.title` | string |  |
| `refundable` | boolean |  |
| `retryable` | boolean |  |
| `status` | string |  |
| `substatus` | string |  |
| `total` | number |  |
| `user` | object |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |
| `voidable` | boolean |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/payments` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

