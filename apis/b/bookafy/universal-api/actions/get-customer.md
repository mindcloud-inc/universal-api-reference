# Bookafy: Get Customer

Retrieves a customer from Bookafy.

```
GET https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=2980611" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2980611"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/get-customer?${params}`, {
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
| `id` | number | yes | Customer ID from Bookafy. Example: `2980611`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "customer": {
          "colorPattern": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerDetailHstore": {
            "email": "ava@example.com",
            "firstName": "Ava",
            "lastName": "Chen",
            "name": "Ava Chen",
            "phone": "string"
          },
          "id": 1,
          "isFake": true,
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
| `response.customer.colorPattern` | string | Customer color pattern. |
| `response.customer.createdAt` | date | Customer creation timestamp. |
| `response.customer.customerDetailHstore.email` | string | Customer email stored in detail fields. |
| `response.customer.customerDetailHstore.firstName` | string | Customer first name stored in detail fields. |
| `response.customer.customerDetailHstore.lastName` | string | Customer last name stored in detail fields. |
| `response.customer.customerDetailHstore.name` | string | Customer display name stored in detail fields. |
| `response.customer.customerDetailHstore.phone` | string | Customer phone stored in detail fields. |
| `response.customer.id` | number | Customer ID. |
| `response.customer.isFake` | boolean | Whether the customer is marked as fake. |
| `response.customer.softDelete` | boolean | Whether the customer is soft-deleted. |
| `response.customer.updatedAt` | date | Customer update timestamp. |
| `response.message` | string | Bookafy status message for the get request. |

## Native endpoint

Through the native Bookafy API, this operation is `GET /customers/:id` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

