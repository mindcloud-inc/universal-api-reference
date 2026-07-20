# Extruct AI: Delete Table Rows

Deletes table rows from Extruct AI.

```
DELETE https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-rows?connectionId=$CONNECTION_ID&tableId=string&rows%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string",
  "rows[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/delete-table-rows?${params}`, {
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
| `tableId` | string | yes | Target table identifier. |
| `rows[]` | array<string> | yes | Array of row IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `DELETE /v1/tables/:table_id/rows` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-rows.md) for the provider-specific parameters and requirements.

