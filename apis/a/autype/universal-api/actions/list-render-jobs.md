# Autype: List Render Jobs

Retrieves render jobs from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-render-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-render-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-render-jobs?${params}`, {
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
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "jobs": [
        {
          "completedAt": "2026-05-07T12:00:00.000Z",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "downloadUrl": "https://example.com",
          "error": "string",
          "filename": "Ava Chen",
          "format": "string",
          "jobId": "string",
          "progress": 1,
          "status": "string"
        }
      ],
      "limit": 1,
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `jobs[].completedAt` | date |  |
| `jobs[].createdAt` | date |  |
| `jobs[].downloadUrl` | string |  |
| `jobs[].error` | string |  |
| `jobs[].filename` | string |  |
| `jobs[].format` | string |  |
| `jobs[].jobId` | string |  |
| `jobs[].progress` | number |  |
| `jobs[].status` | string |  |
| `limit` | number |  |
| `page` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Autype API, this operation is `GET /render` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-render-jobs.md) for the provider-specific parameters and requirements.

