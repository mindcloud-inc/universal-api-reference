# Crowdin: List File Revisions

Retrieves file revisions from a Crowdin project.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-file-revisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-file-revisions?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=1&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "1",
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-file-revisions?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "fileId": 1,
      "id": 1,
      "info": {},
      "projectId": 1,
      "restoreToRevision": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `fileId` | number |  |
| `id` | number |  |
| `info` | object |  |
| `projectId` | number |  |
| `restoreToRevision` | number |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/files/:fileId/revisions` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-file-revisions.md) for the provider-specific parameters and requirements.

