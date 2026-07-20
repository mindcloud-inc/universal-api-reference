# Snappy: List Collection Products

Retrieves products from a specific Snappy collection.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collection-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collection-products?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionId=string&minBudget=1&maxBudget=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collectionId": "string",
  "minBudget": "1",
  "maxBudget": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/list-collection-products?${params}`, {
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
| `collectionId` | string | yes | Collection ID. |
| `minBudget` | number | yes | Minimum budget. |
| `maxBudget` | number | yes | Maximum budget. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Company ID. |
| `country` | string | no | Country. Default: `US`. |
| `accountId` | string | no | Account ID. |
| `fields[]` | array<string> | no | Additional product fields to include. |
| `skip` | number | no | Number of records to skip for pagination. |
| `limit` | number | no | Maximum number of records to return per page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `GET /collections/{collectionId}/products` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collection-products.md) for the provider-specific parameters and requirements.

