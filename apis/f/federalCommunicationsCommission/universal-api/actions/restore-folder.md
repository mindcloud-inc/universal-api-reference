# Federal Communications Commission: Restore Folder

Restores an FCC OPIF folder.

```
PUT https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/restore-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/restore-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/restore-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_ts": "2026-05-07T12:00:00.000Z",
      "entity_folder_id": "string",
      "entity_id": "string",
      "folder_name": "Ava Chen",
      "folder_path": "string",
      "last_update_ts": "2026-05-07T12:00:00.000Z",
      "parent_folder_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_ts` | date | Folder creation timestamp. |
| `entity_folder_id` | string | Folder identifier. |
| `entity_id` | string | FCC entity identifier. |
| `folder_name` | string | Folder name. |
| `folder_path` | string | Folder path. |
| `last_update_ts` | date | Folder last update timestamp. |
| `parent_folder_id` | string | Parent folder identifier. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `PUT /api/manager/folder/restore.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-folder.md) for the provider-specific parameters and requirements.

