# Customer.io: List Customer Segments

Retrieves segments for a customer in Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-segments?connectionId=$CONNECTION_ID&customerId=customer_id_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "customer_id_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-segments?${params}`, {
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
| `customerId` | string | yes | The ID of the customer to inspect. Example: `customer_id_123`. |
| `idType` | list<string> | no | The type of identifier provided in Customer ID. One of: `cio_id`, `email`, `id`. Example: `id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The segment description. |
| `id` | number | The segment identifier. |
| `name` | string | The segment name. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/customers/:customer_id/segments` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-segments.md) for the provider-specific parameters and requirements.

