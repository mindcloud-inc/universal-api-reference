# Katana: List Customers

Lists customers in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-customers?${params}`, {
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
| `name` | string | no | Filters customers by name |
| `firstName` | string | no | Filters customers by first name |
| `lastName` | string | no | Filters customers by last name |
| `company` | string | no | Filters customers by company |
| `ids[]` | array<number> | no | Filters customers by an array of IDs |
| `email` | string | no | Filters customers by an email |
| `phone` | string | no | Filters customers by a phone number |
| `currency` | string | no | Filters customers by currency |
| `referenceId` | string | no | Filters customers by a reference ID |
| `category` | string | no | Filters customers by a category |
| `includeDeleted` | boolean | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `createdAtMin` | string | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `createdAtMax` | string | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updatedAtMin` | string | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updatedAtMax` | string | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "city": "string",
          "company": "string",
          "country": "string",
          "createdAt": "string",
          "customerId": 1,
          "entityType": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "line1": "string",
          "line2": "string",
          "phone": "string",
          "state": "string",
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "category": "string",
      "comment": "string",
      "company": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultBillingId": 1,
      "defaultShippingId": 1,
      "deletedAt": "string",
      "discountRate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "referenceId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `addresses[].city` | string |  |
| `addresses[].company` | string |  |
| `addresses[].country` | string |  |
| `addresses[].createdAt` | string |  |
| `addresses[].customerId` | number |  |
| `addresses[].entityType` | string |  |
| `addresses[].firstName` | string |  |
| `addresses[].id` | number |  |
| `addresses[].lastName` | string |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].phone` | string |  |
| `addresses[].state` | string |  |
| `addresses[].updatedAt` | string |  |
| `addresses[].zip` | string |  |
| `category` | string |  |
| `comment` | string |  |
| `company` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultBillingId` | number |  |
| `defaultShippingId` | number |  |
| `deletedAt` | string |  |
| `discountRate` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `referenceId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /customers` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

