# Ninox: Delete File

Deletes a file from a Ninox record.

```
DELETE https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-file?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&tableId=A&recordId=1&file=invoice.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_id",
  "dbId": "database_id",
  "tableId": "A",
  "recordId": "1",
  "file": "invoice.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/delete-file?${params}`, {
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
| `teamId` | string | yes | The team ID that owns the target database. Example: `team_id`. |
| `dbId` | string | yes | The Ninox database ID. Example: `database_id`. |
| `tableId` | string | yes | The Ninox table ID. Example: `A`. |
| `recordId` | string | yes | The Ninox record ID. Example: `1`. |
| `file` | string | yes | The Ninox file name. Example: `invoice.pdf`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninox API returns.

## Native endpoint

Through the native Ninox API, this operation is `DELETE teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files/:file` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

