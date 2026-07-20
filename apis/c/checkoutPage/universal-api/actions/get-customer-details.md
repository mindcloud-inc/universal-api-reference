# Checkout Page: Get Customer Details

Retrieves customer details from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-customer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-customer-details?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/get-customer-details?${params}`, {
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
| `customerId` | string | yes | Get customer details |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "billingEmail": "ava@example.com",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "sellerId": "string",
      "shipping": {},
      "stripeCustomerId": "string",
      "taxId": "string",
      "taxIdType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `billingEmail` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `sellerId` | string |  |
| `shipping` | object |  |
| `stripeCustomerId` | string |  |
| `taxId` | string |  |
| `taxIdType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/customers/:customerId` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-details.md) for the provider-specific parameters and requirements.

