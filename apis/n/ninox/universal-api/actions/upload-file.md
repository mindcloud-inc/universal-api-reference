# Ninox: Upload File

Uploads a file to a Ninox record.

```
POST https://connect.mindcloud.co/v1/universal/ninox/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "team_id",
  "dbId": "database_id",
  "tableId": "A",
  "recordId": "1",
  "file": "image.jpeg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninox/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "team_id",
    "dbId": "database_id",
    "tableId": "A",
    "recordId": "1",
    "file": "image.jpeg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The team ID that owns the target database. Example: `team_id`. |
| `dbId` | string | yes | The Ninox database ID. Example: `database_id`. |
| `tableId` | string | yes | The Ninox table ID. Example: `A`. |
| `recordId` | string | yes | The Ninox record ID. Example: `1`. |
| `file` | file | yes | The file to upload as multipart/form-data. Example: `image.jpeg`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninox API returns.

## Native endpoint

Through the native Ninox API, this operation is `POST teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

