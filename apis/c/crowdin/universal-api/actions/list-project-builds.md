# Crowdin: List Project Builds

Retrieves project builds from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-builds?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-project-builds?${params}`, {
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
| `branchId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "progress": 1,
      "projectId": 1,
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | date |  |
| `finishedAt` | date |  |
| `id` | number |  |
| `progress` | number |  |
| `projectId` | number |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/translations/builds` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-builds.md) for the provider-specific parameters and requirements.

