# Bookafy: Create Customer

Creates a customer in Bookafy.

```
POST https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer.name": "Jane Smith"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer.name": "Jane Smith"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.name` | string | yes | Customer name. Example: `Jane Smith`. |
| `customer.email` | string | no | Customer email. Example: `jane@example.com`. |
| `customer.phone` | string | no | Customer phone. Example: `+15555550101`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "customer": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerDetailHstore": {
            "phone": "string"
          },
          "email": "ava@example.com",
          "id": 1,
          "name": "Ava Chen",
          "softDelete": true,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.customer.createdAt` | date | Customer creation timestamp. |
| `response.customer.customerDetailHstore.phone` | string | Customer phone number stored in detail fields. |
| `response.customer.email` | string | Customer email address. |
| `response.customer.id` | number | Created customer ID. |
| `response.customer.name` | string | Customer display name. |
| `response.customer.softDelete` | boolean | Whether the customer is soft-deleted. |
| `response.customer.updatedAt` | date | Customer update timestamp. |
| `response.message` | string | Bookafy status message for the create request. |

## Native endpoint

Through the native Bookafy API, this operation is `POST /customers` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

