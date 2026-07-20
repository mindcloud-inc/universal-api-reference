# Ninox: List File Metadata

Retrieves metadata for files in a Ninox record.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-file-metadata?connectionId=$CONNECTION_ID&teamId=team_id&dbId=database_id&tableId=A&recordId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_id",
  "dbId": "database_id",
  "tableId": "A",
  "recordId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/list-file-metadata?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "modifiedDate": 1,
      "modifiedUser": "string",
      "name": "Ava Chen",
      "seq": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | File MIME type. |
| `modifiedDate` | number | Last modified timestamp in milliseconds. |
| `modifiedUser` | string | User who last modified the file. |
| `name` | string | File name. |
| `seq` | number | File sequence number. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-metadata.md) for the provider-specific parameters and requirements.

