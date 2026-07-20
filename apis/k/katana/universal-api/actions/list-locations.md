# Katana: List Locations

Lists locations in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-locations?${params}`, {
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
| `ids[]` | array<number> | no | Filters locations by an array of IDs |
| `name` | string | no | Filters locations by a name |
| `legalName` | string | no | Filters locations by a legal_name |
| `addressId` | number | no | Filters locations by an address_id |
| `salesAllowed` | boolean | no | Filters locations by a sales_allowed |
| `manufacturingAllowed` | boolean | no | Filters locations by a manufacturing_allowed |
| `purchasesAllowed` | boolean | no | Filters locations by a purchases_allowed |
| `rank` | number | no | Filters locations by a rank |
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
      "address": {
        "city": "string",
        "country": "string",
        "id": 1,
        "line1": "string",
        "line2": "string",
        "state": "string",
        "zip": "string"
      },
      "addressId": 1,
      "createdAt": "string",
      "deletedAt": "string",
      "id": 1,
      "isPrimary": true,
      "legalName": "Ava Chen",
      "manufacturingAllowed": true,
      "name": "Ava Chen",
      "purchaseAllowed": true,
      "salesAllowed": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.id` | number |  |
| `address.line1` | string |  |
| `address.line2` | string |  |
| `address.state` | string |  |
| `address.zip` | string |  |
| `addressId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `isPrimary` | boolean |  |
| `legalName` | string |  |
| `manufacturingAllowed` | boolean |  |
| `name` | string |  |
| `purchaseAllowed` | boolean |  |
| `salesAllowed` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /locations` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

