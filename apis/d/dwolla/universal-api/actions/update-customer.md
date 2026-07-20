# Dwolla: Update Customer

Updates an existing customer in Dwolla.

```
PUT https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Dwolla customer ID. |
| `firstName` | string | no | Updated customer first name |
| `lastName` | string | no | Updated customer last name |
| `email` | string | no | Updated customer email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "created": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related customer resources. |
| `created` | string | Customer creation timestamp. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `id` | string | Dwolla customer identifier. |
| `lastName` | string | Customer last name. |
| `status` | string | Customer status. |
| `type` | string | Dwolla customer type. |

## Native endpoint

Through the native Dwolla API, this operation is `POST /customers/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

