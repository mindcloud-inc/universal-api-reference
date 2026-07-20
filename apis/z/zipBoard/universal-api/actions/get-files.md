# zipBoard: Get Files

Retrieves files from zipBoard.

```
GET https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-files?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-files?${params}`, {
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
| `owner` | boolean | no | Return files created by the authenticated user. |
| `projectId` | string | no | Optional project ID to return files for. |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "fileDescription": "string",
      "filePath": "string",
      "Id": "string",
      "orgId": "string",
      "projectId": "string",
      "taskCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `fileDescription` | string |  |
| `filePath` | string |  |
| `Id` | string |  |
| `orgId` | string |  |
| `projectId` | string |  |
| `taskCount` | number |  |

## Native endpoint

Through the native zipBoard API, this operation is `GET /files` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-files.md) for the provider-specific parameters and requirements.

