# Grist: Delete Column

Deletes a column from a Grist table.

```
DELETE https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-column?connectionId=$CONNECTION_ID&docId=string&tableId=string&colId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableId": "string",
  "colId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/delete-column?${params}`, {
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
| `docId` | string | yes | Document ID |
| `tableId` | string | yes | Table ID (e.g. Table1) |
| `colId` | string | yes | Column ID to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body. Grist docs for DELETE /docs/{docId}/tables/{tableId}/columns/{colId} document HTTP 200 with 'Nothing returned'. |

## Native endpoint

Through the native Grist API, this operation is `DELETE /docs/:docId/tables/:tableId/columns/:colId` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-column.md) for the provider-specific parameters and requirements.

