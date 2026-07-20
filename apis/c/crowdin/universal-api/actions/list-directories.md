# Crowdin: List Directories

Retrieves directories from a Crowdin project.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-directories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-directories?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-directories?${params}`, {
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
| `orderBy` | string | no |  |
| `branchId` | number | no |  |
| `directoryId` | number | no |  |
| `filter` | string | no |  |
| `recursion` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "directoryId": 1,
      "exportPattern": "string",
      "id": 1,
      "name": "Ava Chen",
      "path": "string",
      "priority": "string",
      "projectId": 1,
      "title": "string",
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
| `createdAt` | date |  |
| `directoryId` | number |  |
| `exportPattern` | string |  |
| `id` | number |  |
| `name` | string |  |
| `path` | string |  |
| `priority` | string |  |
| `projectId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/directories` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-directories.md) for the provider-specific parameters and requirements.

