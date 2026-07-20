# ImageKit.io: Rename Folder

Starts a folder rename job in ImageKit.io.

```
PUT https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/rename-folder', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderPath` | string | no | Default: `/codex-folder-rename-src`. |
| `newFolderName` | string | no | Default: `codex-folder-renamed-dest`. |
| `purgeCache` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `POST /bulkJobs/renameFolder` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-folder.md) for the provider-specific parameters and requirements.

