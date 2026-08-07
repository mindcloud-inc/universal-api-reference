# Shopify: Get Inventory Bulk Export Status



```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-inventory-bulk-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-inventory-bulk-export-status?connectionId=$CONNECTION_ID&variables.id=gid%3A%2F%2Fshopify%2FBulkOperation%2F%E2%80%A6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "gid://shopify/BulkOperation/…"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/get-inventory-bulk-export-status?${params}`, {
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
| `variables` | object | no |  |
| `variables.id` | string | yes | The bulk operation ID returned by Start Inventory Bulk Export, for example gid://shopify/BulkOperation/720918. Example: `gid://shopify/BulkOperation/…`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-bulk-export-status.md) for the provider-specific parameters and requirements.

