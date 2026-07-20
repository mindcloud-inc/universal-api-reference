# Linear: List Issues

Search Linear Issues.

```
GET https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linear `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-issues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-issues?${params}`, {
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
| `team` | list | no |  |
| `title` | string | no |  |
| `state` | string | no |  |
| `createdAfter` | date | no | Filter issues to return only those created after a specific date. |
| `updatedAfter` | date | no |  |
| `project` | string | no | The project that this issue is a part of. |
| `projectState` | string | no | The status of the Project this Issue is a part of. |
| `titleContains` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activitySummary": {},
      "addedToCycleAt": {},
      "addedToProjectAt": "string",
      "addedToTeamAt": "string",
      "archivedAt": {},
      "autoArchivedAt": {},
      "autoClosedAt": {},
      "boardOrder": 1,
      "branchName": "Ava Chen",
      "canceledAt": {},
      "completedAt": {},
      "createdAt": "string",
      "customerTicketCount": 1,
      "description": "string",
      "dueDate": {},
      "estimate": {},
      "id": "string",
      "identifier": "string",
      "integrationSourceType": {},
      "number": 1,
      "priority": 1,
      "priorityLabel": "string",
      "prioritySortOrder": 1,
      "slaBreachesAt": {},
      "slaHighRiskAt": {},
      "slaMediumRiskAt": {},
      "slaStartedAt": {},
      "slaType": "string",
      "startedAt": {},
      "startedTriageAt": {},
      "subIssueSortOrder": {},
      "suggestionsGeneratedAt": {},
      "title": "string",
      "trashed": {},
      "triagedAt": {},
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activitySummary` | object |  |
| `addedToCycleAt` | object |  |
| `addedToProjectAt` | string |  |
| `addedToTeamAt` | string |  |
| `archivedAt` | object |  |
| `autoArchivedAt` | object |  |
| `autoClosedAt` | object |  |
| `boardOrder` | number |  |
| `branchName` | string |  |
| `canceledAt` | object |  |
| `completedAt` | object |  |
| `createdAt` | string |  |
| `customerTicketCount` | number |  |
| `description` | string |  |
| `dueDate` | object |  |
| `estimate` | object |  |
| `id` | string |  |
| `identifier` | string |  |
| `integrationSourceType` | object |  |
| `number` | number |  |
| `priority` | number |  |
| `priorityLabel` | string |  |
| `prioritySortOrder` | number |  |
| `slaBreachesAt` | object |  |
| `slaHighRiskAt` | object |  |
| `slaMediumRiskAt` | object |  |
| `slaStartedAt` | object |  |
| `slaType` | string |  |
| `startedAt` | object |  |
| `startedTriageAt` | object |  |
| `subIssueSortOrder` | object |  |
| `suggestionsGeneratedAt` | object |  |
| `title` | string |  |
| `trashed` | object |  |
| `triagedAt` | object |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Linear API, this operation is `POST` (base URL `https://api.linear.app/graphql/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

