# Crowdin: Get File

Retrieves a file from a Crowdin project.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-file?connectionId=$CONNECTION_ID&projectId=1&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/get-file?${params}`, {
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
| `projectId` | number | yes |  |
| `fileId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "directoryId": 1,
      "excludedTargetLanguages": [
        "string"
      ],
      "exportOptions": {},
      "id": 1,
      "importOptions": {},
      "name": "Ava Chen",
      "parserVersion": 1,
      "path": "string",
      "priority": "string",
      "projectId": 1,
      "revisionId": 1,
      "status": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number |  |
| `context` | string |  |
| `createdAt` | date |  |
| `directoryId` | number |  |
| `excludedTargetLanguages` | array<string> |  |
| `exportOptions` | object |  |
| `id` | number |  |
| `importOptions` | object |  |
| `name` | string |  |
| `parserVersion` | number |  |
| `path` | string |  |
| `priority` | string |  |
| `projectId` | number |  |
| `revisionId` | number |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/files/:fileId` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

