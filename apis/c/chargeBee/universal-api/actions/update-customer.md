# ChargeBee: Update Customer

Updates an existing customer in ChargeBee.

```
PUT https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer_id` | string | yes | The unique identifier of the Chargebee customer to update. |
| `first_name` | string | no | Updated customer first name. |
| `last_name` | string | no | Updated customer last name. |
| `email` | string | no | Updated customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "object": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `created_at` | number |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `object` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `POST customers/:customer_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

