# Pabbly Subscription Billing: Get Single Customer via Customer ID



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-customer-via-customer-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-customer-via-customer-id?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-customer-via-customer-id?${params}`, {
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
| `customerId` | string | yes | Pabbly customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {
        "attention": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phone": "string",
      "shippingAddress": {
        "attention": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress.attention` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.street1` | string |  |
| `billingAddress.street2` | string |  |
| `billingAddress.zipCode` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `shippingAddress.attention` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.state` | string |  |
| `shippingAddress.street1` | string |  |
| `shippingAddress.street2` | string |  |
| `shippingAddress.zipCode` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/customer/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-customer-via-customer-id.md) for the provider-specific parameters and requirements.

