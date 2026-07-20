# Federal Communications Commission: Rename File

Updates the name of an FCC OPIF file.

```
PUT https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/rename-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/rename-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/rename-file', {
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
      "file_extension": "string",
      "file_id": "string",
      "file_manager_id": "string",
      "file_name": "Ava Chen",
      "file_size": 1,
      "file_status": "string",
      "folder_id": "string",
      "last_update_ts": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_ts` | date | File creation timestamp. |
| `file_extension` | string | File extension. |
| `file_id` | string | File identifier. |
| `file_manager_id` | string | File manager identifier. |
| `file_name` | string | File name. |
| `file_size` | number | File size. |
| `file_status` | string | File status. |
| `folder_id` | string | Folder identifier. |
| `last_update_ts` | date | File last update timestamp. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `PUT /api/manager/file/rename.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-file.md) for the provider-specific parameters and requirements.

