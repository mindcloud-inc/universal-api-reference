# SweetProcess: List Procedures

Retrieves procedures from SweetProcess.

```
GET https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SweetProcess `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sweetProcess/latest/actions/list-procedures?${params}`, {
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
| `search` | string | no | Full-text search for procedures. |
| `teamId` | number | no | Filter procedures within the given team. |
| `tag` | string | no | Comma-separated tag names to filter procedures. |
| `policyId` | number | no | Filter procedures attached to the given policy. |
| `visibleToUser` | string | no | Filter procedures visible to both the current user and the referenced user URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "approvedAt": "2026-05-07T12:00:00.000Z",
      "approvedBy": {},
      "author": {},
      "canAssign": true,
      "canChange": true,
      "canDelete": true,
      "canEdit": true,
      "canExport": true,
      "connections": [
        {}
      ],
      "content": "string",
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentVersion": {},
      "description": {},
      "diagramPngStatus": "string",
      "diagramPngUrl": "https://example.com",
      "editedAt": "2026-05-07T12:00:00.000Z",
      "embedUrl": "https://example.com",
      "hashid": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "isLarge": true,
      "lanes": {},
      "lastReviewAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextReviewAt": "2026-05-07T12:00:00.000Z",
      "originalAuthor": {},
      "policies": [
        {}
      ],
      "private": true,
      "processes": [
        {}
      ],
      "reviewer": {},
      "reviewPeriodMonths": 1,
      "signoffRequestedAt": "2026-05-07T12:00:00.000Z",
      "signoffRequestedBy": {},
      "slug": "string",
      "stepsBlockedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "teamMemberships": [
        {}
      ],
      "teamNames": [
        "Ava Chen"
      ],
      "templateAt": "2026-05-07T12:00:00.000Z",
      "thumbnail": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `approvedAt` | date |  |
| `approvedBy` | object |  |
| `author` | object |  |
| `canAssign` | boolean |  |
| `canChange` | boolean |  |
| `canDelete` | boolean |  |
| `canEdit` | boolean |  |
| `canExport` | boolean |  |
| `connections` | array<object> |  |
| `content` | string |  |
| `contentType` | string |  |
| `createdAt` | date |  |
| `currentVersion` | object |  |
| `description` | object |  |
| `diagramPngStatus` | string |  |
| `diagramPngUrl` | string |  |
| `editedAt` | date |  |
| `embedUrl` | string |  |
| `hashid` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `isLarge` | boolean |  |
| `lanes` | object |  |
| `lastReviewAt` | date |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `nextReviewAt` | date |  |
| `originalAuthor` | object |  |
| `policies` | array<object> |  |
| `private` | boolean |  |
| `processes` | array<object> |  |
| `reviewer` | object |  |
| `reviewPeriodMonths` | number |  |
| `signoffRequestedAt` | date |  |
| `signoffRequestedBy` | object |  |
| `slug` | string |  |
| `stepsBlockedAt` | date |  |
| `tags` | array<string> |  |
| `teamMemberships` | array<object> |  |
| `teamNames` | array<string> |  |
| `templateAt` | date |  |
| `thumbnail` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SweetProcess API, this operation is `GET /procedures/` (base URL `https://www.sweetprocess.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-procedures.md) for the provider-specific parameters and requirements.

