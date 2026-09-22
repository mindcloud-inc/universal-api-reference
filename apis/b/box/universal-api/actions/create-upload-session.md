# Box: Create Upload Session



```
POST https://connect.mindcloud.co/v1/universal/box/latest/actions/create-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/box/latest/actions/create-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "0",
  "fileSize": "1048576",
  "fileName": "report.csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/create-upload-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "0",
    "fileSize": "1048576",
    "fileName": "report.csv"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Parent Box folder ID. Use `0` for the root folder. Default: `0`. Example: `0`. |
| `fileSize` | number | yes | Total file size in bytes, not the length of its base64 representation. Example: `1048576`. |
| `fileName` | string | yes | Name of the file to upload. Example: `report.csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "numPartsProcessed": 1,
      "partSize": 1,
      "sessionEndpoints": {
        "abort": "string",
        "commit": "string",
        "listParts": "string",
        "logEvent": "string",
        "plan": "string",
        "status": "string",
        "uploadPart": "string"
      },
      "sessionExpiresAt": "string",
      "totalParts": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `numPartsProcessed` | number |  |
| `partSize` | number |  |
| `sessionEndpoints.abort` | string |  |
| `sessionEndpoints.commit` | string |  |
| `sessionEndpoints.listParts` | string |  |
| `sessionEndpoints.logEvent` | string |  |
| `sessionEndpoints.plan` | string |  |
| `sessionEndpoints.status` | string |  |
| `sessionEndpoints.uploadPart` | string |  |
| `sessionExpiresAt` | string |  |
| `totalParts` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Box API, this operation is `POST https://upload.box.com/api/2.0/files/upload_sessions`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-session.md) for the provider-specific parameters and requirements.

