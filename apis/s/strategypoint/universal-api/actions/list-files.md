# Strategypoint: List Files

Retrieves files from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-files?${params}`, {
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
| `count` | number | no | Maximum number of files to return. |
| `search` | string | no | Search text to match files. |
| `start` | number | no | Offset into the file result set. |
| `userId` | number | no | Filter files by the uploading user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileCount": 1,
      "fileName": "Ava Chen",
      "files": [
        {}
      ],
      "filetype": "string",
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
| `fileCount` | number | The number of files returned. |
| `fileName` | string | The stored file name. |
| `files` | array<object> | The file records returned by the API. |
| `filetype` | string | The file type. |
| `name` | string | The display name of the file. |
| `scorecardId` | number | The related scorecard identifier. |
| `uploadDate` | string | The upload timestamp. |
| `userId` | number | The uploading user identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /files` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

