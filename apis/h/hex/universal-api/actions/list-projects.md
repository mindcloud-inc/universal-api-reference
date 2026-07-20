# Hex: List Projects



```
GET https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-projects?${params}`, {
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
| `includeArchived` | boolean | no | Whether to include archived projects. |
| `includeComponents` | boolean | no | Whether to include components in the results. |
| `includeTrashed` | boolean | no | Whether to include trashed projects. |
| `includeSharing` | boolean | no | Whether to include sharing details in each project. |
| `statuses[]` | array<string> | no | Filter projects by status name. |
| `categories[]` | array<string> | no | Filter projects by category name. |
| `creatorEmail` | string | no | Filter projects by creator email. |
| `ownerEmail` | string | no | Filter projects by owner email. |
| `collectionId` | string | no | Filter projects by collection ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics": {
        "appViews": {
          "allTime": 1,
          "lastFourteenDays": 1,
          "lastSevenDays": 1,
          "lastThirtyDays": 1
        },
        "lastViewedAt": "2026-05-07T12:00:00.000Z",
        "publishedResultsUpdatedAt": "2026-05-07T12:00:00.000Z"
      },
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "categories": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creator": {
        "email": "ava@example.com"
      },
      "description": "string",
      "id": "string",
      "lastEditedAt": "2026-05-07T12:00:00.000Z",
      "lastPublishedAt": "2026-05-07T12:00:00.000Z",
      "owner": {
        "email": "ava@example.com"
      },
      "reviews": {
        "required": true
      },
      "schedules": [
        {}
      ],
      "status": "string",
      "title": "string",
      "trashedAt": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics.appViews.allTime` | number |  |
| `analytics.appViews.lastFourteenDays` | number |  |
| `analytics.appViews.lastSevenDays` | number |  |
| `analytics.appViews.lastThirtyDays` | number |  |
| `analytics.lastViewedAt` | date |  |
| `analytics.publishedResultsUpdatedAt` | date |  |
| `archivedAt` | date |  |
| `categories` | array<string> | Retrieves projects from Hex. |
| `createdAt` | date |  |
| `creator.email` | string |  |
| `description` | string |  |
| `id` | string |  |
| `lastEditedAt` | date |  |
| `lastPublishedAt` | date |  |
| `owner.email` | string |  |
| `reviews.required` | boolean |  |
| `schedules` | array<object> | Retrieves a project from Hex. |
| `status` | string |  |
| `title` | string |  |
| `trashedAt` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Hex API, this operation is `GET /projects` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

