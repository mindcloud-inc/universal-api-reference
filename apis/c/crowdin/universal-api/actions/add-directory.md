# Crowdin: Add Directory

Creates a new directory in a Crowdin project.

```
POST https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/add-directory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
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
| `name` | string | yes |  |
| `branchId` | number | no |  |
| `directoryId` | number | no |  |
| `title` | string | no |  |
| `exportPattern` | string | no |  |
| `priority` | string | no | Default: `normal`. |

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

Through the native Crowdin API, this operation is `POST /projects/:projectId/directories` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-directory.md) for the provider-specific parameters and requirements.

