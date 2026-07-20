# TimelinesAI: Get File

Retrieves details for an uploaded TimelinesAI file.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-file?connectionId=$CONNECTION_ID&fileUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-file?${params}`, {
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
| `fileUid` | string | yes | UID of the uploaded file in the TimelinesAI workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "filename": "Ava Chen",
        "mimetype": "string",
        "size": 1,
        "temporaryDownloadUrl": "https://example.com",
        "uid": "string",
        "uploadedAt": "string",
        "uploadedByEmail": "ava@example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.filename` | string |  |
| `data.mimetype` | string |  |
| `data.size` | number |  |
| `data.temporaryDownloadUrl` | string |  |
| `data.uid` | string |  |
| `data.uploadedAt` | string |  |
| `data.uploadedByEmail` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /files/{file_uid}` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

