# Bookafy: List Customers

Retrieves customers from Bookafy.

```
GET https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "customers": [
          {
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
          }
        ],
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
| `response.customers[].colorPattern` | string | Customer color pattern. |
| `response.customers[].createdAt` | date | Customer creation timestamp. |
| `response.customers[].customerDetailHstore.email` | string | Customer email stored in detail fields. |
| `response.customers[].customerDetailHstore.firstName` | string | Customer first name stored in detail fields. |
| `response.customers[].customerDetailHstore.lastName` | string | Customer last name stored in detail fields. |
| `response.customers[].customerDetailHstore.name` | string | Customer display name stored in detail fields. |
| `response.customers[].customerDetailHstore.phone` | string | Customer phone stored in detail fields. |
| `response.customers[].id` | number | Customer ID. |
| `response.customers[].isFake` | boolean | Whether the customer is marked as fake. |
| `response.customers[].softDelete` | boolean | Whether the customer is soft-deleted. |
| `response.customers[].updatedAt` | date | Customer update timestamp. |
| `response.message` | string | Bookafy status message for the list request. |

## Native endpoint

Through the native Bookafy API, this operation is `GET /customers` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

