# Baserow: Delete Row

Deletes an existing row from Baserow.

```
DELETE https://connect.mindcloud.co/v1/universal/baserow/latest/actions/delete-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/delete-row?connectionId=$CONNECTION_ID&tableId=1&rowId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "1",
  "rowId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/delete-row?${params}`, {
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
| `tableId` | number | yes | The Baserow table containing the row. |
| `rowId` | number | yes | The row to delete. |
| `sendWebhookEvents` | boolean | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | number | no | Optional view context for permissions and default values. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Baserow API returns.

## Native endpoint

Through the native Baserow API, this operation is `DELETE /api/database/rows/table/:table_id/:row_id/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-row.md) for the provider-specific parameters and requirements.

