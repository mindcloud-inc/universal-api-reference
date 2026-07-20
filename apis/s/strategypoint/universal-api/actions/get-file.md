# Strategypoint: Get File

Retrieves a file from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-file?${params}`, {
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
| `fileId` | number | yes | The unique file identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileExists": true,
      "fileName": "Ava Chen",
      "filetype": "string",
      "link": {},
      "name": "Ava Chen",
      "scorecardId": 1,
      "uploadDate": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileExists` | boolean | Whether the file exists. |
| `fileName` | string | The stored file name. |
| `filetype` | string | The file type. |
| `link` | object | Link metadata for the file. |
| `name` | string | The display name of the file. |
| `scorecardId` | number | The related scorecard identifier. |
| `uploadDate` | string | The upload timestamp. |
| `userId` | number | The uploading user identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /files/{fileId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

