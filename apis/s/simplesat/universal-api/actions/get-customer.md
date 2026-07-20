# Simplesat: Get Customer

Retrieves a customer from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-customer?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The ID of the customer to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "custom_attributes": {},
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `custom_attributes` | object |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/customers/:customer_id` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

