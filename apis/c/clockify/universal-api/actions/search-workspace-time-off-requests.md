# Clockify: Search Workspace Time Off Requests

Finds workspace time off requests in Clockify by filters.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-time-off-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-time-off-requests?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/search-workspace-time-off-requests?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `end` | date | no | Example: `2026-01-01T00:00:00Z`. |
| `page` | number | no | Example: `100`. |
| `pageSize` | number | no | Example: `100`. |
| `start` | date | no | Example: `2026-01-01T00:00:00Z`. |
| `statuses[]` | array<string> | no |  |
| `userGroups[]` | array<string> | no |  |
| `users[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "requests": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `requests[]` | array<object> |  |
| `requests[].balance` | number |  |
| `requests[].balanceDiff` | number |  |
| `requests[].createdAt` | date |  |
| `requests[].id` | string |  |
| `requests[].note` | string |  |
| `requests[].policyId` | string |  |
| `requests[].policyName` | string |  |
| `requests[].requesterUserId` | string |  |
| `requests[].requesterUserName` | string |  |
| `requests[].status` | object |  |
| `requests[].status.changedAt` | date |  |
| `requests[].status.changedByUserId` | string |  |
| `requests[].status.changedByUserName` | string |  |
| `requests[].status.changedForUserName` | string |  |
| `requests[].status.note` | string |  |
| `requests[].status.statusType` | string |  |
| `requests[].timeOffPeriod` | object |  |
| `requests[].timeOffPeriod.halfDay` | boolean |  |
| `requests[].timeOffPeriod.halfDayHours` | object |  |
| `requests[].timeOffPeriod.halfDayHours.end` | date |  |
| `requests[].timeOffPeriod.halfDayHours.start` | date |  |
| `requests[].timeOffPeriod.halfDayPeriod` | string |  |
| `requests[].timeOffPeriod.period` | object |  |
| `requests[].timeOffPeriod.period.end` | date |  |
| `requests[].timeOffPeriod.period.start` | date |  |
| `requests[].timeUnit` | string |  |
| `requests[].userEmail` | string |  |
| `requests[].userId` | string |  |
| `requests[].userName` | string |  |
| `requests[].userTimeZone` | string |  |
| `requests[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/time-off/requests` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workspace-time-off-requests.md) for the provider-specific parameters and requirements.

