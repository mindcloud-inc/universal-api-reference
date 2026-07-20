# Catalog Machine: Delete Products (Bulk)

Deletes multiple products from Catalog Machine.

```
DELETE https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/delete-products-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Catalog Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/delete-products-bulk?connectionId=$CONNECTION_ID&codes%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codes[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/delete-products-bulk?${params}`, {
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
| `codes[]` | array<string> | yes | Array of product codes to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Catalog Machine API returns.

## Native endpoint

Through the native Catalog Machine API, this operation is `DELETE /products` (base URL `https://www.catalogmachine.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-products-bulk.md) for the provider-specific parameters and requirements.

