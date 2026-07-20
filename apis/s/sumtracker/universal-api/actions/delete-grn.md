# Sumtracker: Delete Goods Receipt Note

Deletes a goods receipt note from Sumtracker.

```
DELETE https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-grn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-grn?connectionId=$CONNECTION_ID&document_type=string&id=string&po_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_type": "string",
  "id": "string",
  "po_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-grn?${params}`, {
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
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | string | yes | Goods receipt note ID. |
| `po_id` | string | yes | Purchase order or stock transfer ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `DELETE /api/version/2025-03/purchases/:document_type/:po_id/grns/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-grn.md) for the provider-specific parameters and requirements.

