# Katana: List Suppliers

Lists suppliers in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-suppliers?${params}`, {
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
| `name` | string | no | Filters suppliers by name |
| `ids[]` | array<number> | no | Filters suppliers by an array of IDs |
| `email` | string | no | Filters suppliers by an email |
| `phone` | string | no | Filters suppliers by a phone number |
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
          "country": "string",
          "createdAt": "string",
          "id": 1,
          "line1": "string",
          "line2": "string",
          "state": "string",
          "supplierId": 1,
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "comment": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultAddressId": 1,
      "deletedAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
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
| `addresses[].country` | string |  |
| `addresses[].createdAt` | string |  |
| `addresses[].id` | number |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].state` | string |  |
| `addresses[].supplierId` | number |  |
| `addresses[].updatedAt` | string |  |
| `addresses[].zip` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultAddressId` | number |  |
| `deletedAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /suppliers` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

