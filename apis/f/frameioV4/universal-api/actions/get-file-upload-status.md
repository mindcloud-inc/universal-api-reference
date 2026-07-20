# Frame.io v4: Get File Upload Status

Retrieves file upload status from Frame.io v4.

```
GET https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file-upload-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frame.io v4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file-upload-status?connectionId=$CONNECTION_ID&accountId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameioV4/latest/actions/get-file-upload-status?${params}`, {
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
| `accountId` | string | yes |  |
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filetype": "string",
      "id": "string",
      "uploadComplete": true,
      "uploadCompletedAt": "2026-05-07T12:00:00.000Z",
      "uploadedAt": "2026-05-07T12:00:00.000Z",
      "uploadFailed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filetype` | string | File type |
| `id` | string | File ID |
| `uploadComplete` | boolean | Indicates if upload is complete |
| `uploadCompletedAt` | date | Timestamp when the asset was successfully uploaded |
| `uploadedAt` | date | Timestamp when the operation started |
| `uploadFailed` | boolean | Indicates if upload failed |

## Native endpoint

Through the native Frame.io v4 API, this operation is `GET /accounts/:accountId/files/:fileId/status` (base URL `https://api.frame.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-upload-status.md) for the provider-specific parameters and requirements.

