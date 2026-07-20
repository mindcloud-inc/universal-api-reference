# Mendato: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/mendato/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendato/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | Required GraphQL variables object with an input payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateCustomer": {
        "customer": {
          "addressSupplement": "string",
          "companyName": "Ava Chen",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "number": 1,
          "salutation": "string",
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateCustomer.customer.addressSupplement` | string |  |
| `updateCustomer.customer.companyName` | string |  |
| `updateCustomer.customer.firstName` | string |  |
| `updateCustomer.customer.id` | string |  |
| `updateCustomer.customer.lastName` | string |  |
| `updateCustomer.customer.number` | number |  |
| `updateCustomer.customer.salutation` | string |  |
| `updateCustomer.customer.type` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

