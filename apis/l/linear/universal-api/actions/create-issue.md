# Linear: Create Issue

Create Linear Issue.

```
POST https://connect.mindcloud.co/v1/universal/linear/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linear/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linear/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | list | no |  |
| `title` | string | no |  |
| `description` | string | no |  |

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

Through the native Linear API, this operation is `POST` (base URL `https://api.linear.app/graphql/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

