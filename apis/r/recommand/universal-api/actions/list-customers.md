# Recommand: List Customers

Retrieves customer records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-customers?${params}`, {
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
| `search` | string | no | search parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "address": "string",
          "city": "string",
          "country": "string",
          "createdAt": "string",
          "email": "ava@example.com",
          "enterpriseNumber": "string",
          "externalId": "string",
          "id": "string",
          "name": "Ava Chen",
          "peppolAddresses": [
            "string"
          ],
          "phone": "string",
          "postalCode": "string",
          "teamId": "string",
          "updatedAt": "string",
          "vatNumber": "string"
        }
      ],
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1,
        "totalPages": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `customers[].address` | string |  |
| `customers[].city` | string |  |
| `customers[].country` | string |  |
| `customers[].createdAt` | string |  |
| `customers[].email` | string |  |
| `customers[].enterpriseNumber` | string |  |
| `customers[].externalId` | string |  |
| `customers[].id` | string |  |
| `customers[].name` | string |  |
| `customers[].peppolAddresses` | array<string> |  |
| `customers[].phone` | string |  |
| `customers[].postalCode` | string |  |
| `customers[].teamId` | string |  |
| `customers[].updatedAt` | string |  |
| `customers[].vatNumber` | string |  |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/customers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

