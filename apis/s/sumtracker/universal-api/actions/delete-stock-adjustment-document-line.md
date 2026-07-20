# Sumtracker: Delete Stock Adjustment Document Line

Deletes a stock adjustment document line from Sumtracker.

```
DELETE https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-stock-adjustment-document-line
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-stock-adjustment-document-line?connectionId=$CONNECTION_ID&document_id=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/delete-stock-adjustment-document-line?${params}`, {
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
| `document_id` | string | yes | Stock adjustment document ID. |
| `id` | string | yes | Stock adjustment document line ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `DELETE /api/version/2025-03/stock/adjustment/documents/:document_id/lines/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-stock-adjustment-document-line.md) for the provider-specific parameters and requirements.

