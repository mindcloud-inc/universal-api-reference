# Clockify: Get Workspace User Capacity Totals

Retrieves workspace user capacity totals from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-totals?connectionId=$CONNECTION_ID&end=2026-05-07T12%3A00%3A00.000Z&start=2026-05-07T12%3A00%3A00.000Z&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "2026-05-07T12:00:00.000Z",
  "start": "2026-05-07T12:00:00.000Z",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-totals?${params}`, {
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
| `end` | date | yes |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `search` | string | no |  |
| `start` | date | yes |  |
| `statusFilter` | list | no | One of: `ALL`, `PUBLISHED`, `UNPUBLISHED`. |
| `userFilter` | object | no |  |
| `userFilter.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userFilter.ids[]` | array<string> | no |  |
| `userFilter.sourceType` | list | no | One of: `USER_GROUP`. |
| `userFilter.status` | list | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `userFilter.statuses` | list<string> | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. Accepts multiple values as an array. |
| `userFilter.statuses[]` | string | no |  |
| `userGroupFilter` | object | no |  |
| `userGroupFilter.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroupFilter.ids[]` | array<string> | no |  |
| `userGroupFilter.status` | list | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items[]` | array<object> |  |
| `items[].capacityPerDay` | number |  |
| `items[].totalHoursPerDay[]` | array<object> |  |
| `items[].totalHoursPerDay[].date` | date |  |
| `items[].totalHoursPerDay[].totalHours` | number |  |
| `items[].userId` | string |  |
| `items[].userImage` | string |  |
| `items[].userName` | string |  |
| `items[].userStatus` | string |  |
| `items[].workingDays` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/scheduling/assignments/user-filter/totals` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-user-capacity-totals.md) for the provider-specific parameters and requirements.

