# BigCommerce: Create Customer Address



```
POST https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-customer-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-customer-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "last_name": "Chen",
  "address1": "string",
  "city": "string",
  "state_or_province": "string",
  "postal_code": "string",
  "country_code": "string",
  "customer_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-customer-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "last_name": "Chen",
    "address1": "string",
    "city": "string",
    "state_or_province": "string",
    "postal_code": "string",
    "country_code": "string",
    "customer_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | yes |  |
| `last_name` | string | yes |  |
| `company` | string | no |  |
| `address1` | string | yes |  |
| `address2` | string | no |  |
| `city` | string | yes |  |
| `state_or_province` | string | yes |  |
| `postal_code` | string | yes |  |
| `country_code` | string | yes |  |
| `phone` | string | no |  |
| `address_type` | string | no |  |
| `customer_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `POST /v3/customers/addresses` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/create-customer-address.md) for the provider-specific parameters and requirements.

