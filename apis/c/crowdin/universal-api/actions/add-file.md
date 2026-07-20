# Crowdin: Add File

Creates a new file in a Crowdin project.

```
POST https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "storageId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "storageId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `storageId` | number | yes |  |
| `name` | string | yes |  |
| `branchId` | number | no |  |
| `directoryId` | number | no |  |
| `title` | string | no |  |
| `context` | string | no |  |
| `type` | string | no |  |
| `parserVersion` | number | no |  |
| `importOptions` | object | no |  |
| `exportOptions` | object | no |  |
| `excludedTargetLanguages[]` | array<string> | no |  |
| `attachLabelIds[]` | array<number> | no |  |

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

Through the native Crowdin API, this operation is `POST /projects/:projectId/files` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file.md) for the provider-specific parameters and requirements.

