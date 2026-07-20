# GorillaDesk: Update Customer

Updates an existing customer in GorillaDesk.

```
PUT https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountNumber": "string",
  "customerId": "string",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountNumber": "string",
    "customerId": "string",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountNumber` | string | yes |  |
| `company` | string | no |  |
| `customerId` | string | yes | Customer Id |
| `email` | string | no |  |
| `firstName` | string | yes |  |
| `lastName` | string | no |  |
| `phones[]` | array<object> | no |  |
| `phones[].phone` | string | no |  |
| `phones[].type` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `PUT /customers/:customerId` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

