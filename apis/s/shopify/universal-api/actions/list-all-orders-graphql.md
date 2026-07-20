# Shopify: List All Orders

Retrieves orders from Shopify with GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-all-orders-graphql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-all-orders-graphql?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-all-orders-graphql?${params}`, {
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
| `orderQuery` | string | no | Optional Shopify order search query string. Leave blank to list orders. Example: `status:open`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAfter` | string | no | Optional lower bound for Shopify created_at order search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `createdBefore` | string | no | Optional upper bound for Shopify created_at order search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `updatedAfter` | string | no | Optional lower bound for Shopify updated_at order search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `updatedBefore` | string | no | Optional upper bound for Shopify updated_at order search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `financialStatus` | string | no | Optional Shopify financial_status filter, for example paid, pending, authorized, partially_paid, refunded, or voided. Example: `paid`. |
| `names[]` | array<string> | no | Optional list of Shopify order names to match, for example #1001 or 1001. Example: `#1001`. |
| `reverse` | boolean | no | Reverse the sort order of the results. Default: `false`. |
| `afterCursor` | string | no | Optional cursor for manually continuing from a previous page. Standard pagination controls handle this automatically in most workflows. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2025-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-orders-graphql.md) for the provider-specific parameters and requirements.

