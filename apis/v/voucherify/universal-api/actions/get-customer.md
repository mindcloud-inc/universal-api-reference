# Voucherify: Get Customer

Retrieves a customer from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | Voucherify customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "createdAt": "string",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "loyalty": {},
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "referrals": {},
      "sourceId": "string",
      "summary": {},
      "systemMetadata": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `createdAt` | string |  |
| `description` | string |  |
| `email` | string |  |
| `id` | string |  |
| `loyalty` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `referrals` | object |  |
| `sourceId` | string |  |
| `summary` | object |  |
| `systemMetadata` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /customers/:customerId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

