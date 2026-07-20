# Mendato: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-customer?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-customer?${params}`, {
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
| `variables` | object | yes | Required GraphQL variables object with the customer id. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.addressSupplement` | string |  |
| `customer.companyName` | string |  |
| `customer.firstName` | string |  |
| `customer.id` | string |  |
| `customer.lastName` | string |  |
| `customer.number` | number |  |
| `customer.salutation` | string |  |
| `customer.type` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

