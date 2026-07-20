# ImageKit.io: Copy Folder

Starts a folder copy job in ImageKit.io.

```
PUT https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/copy-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/copy-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/copy-folder', {
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
| `destinationPath` | string | no | Default: `/codex-folder-copy-dest`. |
| `includeVersions` | boolean | no |  |
| `sourceFolderPath` | string | no | Default: `/codex-folder-copy-src`. |

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

Through the native ImageKit.io API, this operation is `POST /bulkJobs/copyFolder` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-folder.md) for the provider-specific parameters and requirements.

