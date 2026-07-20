# Bookafy: Update Customer

Updates a customer in Bookafy.

```
PUT https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "2980611",
  "customer.name": "Jane Smith"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "2980611",
    "customer.name": "Jane Smith"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Customer ID from Bookafy. Example: `2980611`. |
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
| `response.customer.id` | number | Customer ID. |
| `response.customer.name` | string | Customer display name. |
| `response.customer.softDelete` | boolean | Whether the customer is soft-deleted. |
| `response.customer.updatedAt` | date | Customer update timestamp. |
| `response.message` | string | Bookafy status message for the update request. |

## Native endpoint

Through the native Bookafy API, this operation is `PUT /customers/:id` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

