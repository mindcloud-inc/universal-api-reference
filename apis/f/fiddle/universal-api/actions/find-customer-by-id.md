# Fiddle: Find Customer by ID

Finds a customer in Fiddle by ID.

```
GET https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-customer-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-customer-by-id?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/find-customer-by-id?${params}`, {
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
| `customerId` | string | yes | Customer ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object |  |
| `customer.createdAt` | date |  |
| `customer.id` | string |  |
| `customer.name` | string |  |
| `customer.updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `GET /customers/:customerId` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-customer-by-id.md) for the provider-specific parameters and requirements.

