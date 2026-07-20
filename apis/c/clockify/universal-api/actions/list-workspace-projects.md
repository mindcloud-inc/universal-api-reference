# Clockify: List Workspace Projects

Lists all workspace projects in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-projects?${params}`, {
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
| `workspaceId` | list<string> | yes | Workspace identifier. |
| `name` | string | no | Filter projects by name. |
| `strictNameSearch` | boolean | no | Return exact project name matches only. |
| `archived` | boolean | no | Filter archived projects. |
| `billable` | boolean | no | Filter billable projects. |
| `clients[]` | array<string> | no | Filter by client IDs. |
| `containsClient` | boolean | no | Include or exclude matching clients. |
| `clientStatus` | string | no | Filter by client status. |
| `users[]` | array<string> | no | Filter by user IDs. |
| `containsUser` | boolean | no | Include or exclude matching users. |
| `userStatus` | string | no | Filter by user status. |
| `isTemplate` | boolean | no | Filter template projects. |
| `hydrated` | boolean | no | Include hydrated project data. |
| `access` | string | no | Project access visibility. |
| `expenseLimit` | number | no | Maximum expenses to include. |
| `expenseDate` | string | no | Include expenses before this date (yyyy-MM-dd). |
| `userGroups[]` | array<string> | no | Filter by user group IDs. |
| `containsGroup` | boolean | no | Include or exclude matching user groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "billable": true,
      "budgetEstimate": {},
      "clientId": "string",
      "clientName": "Ava Chen",
      "color": "string",
      "costRate": {},
      "duration": "string",
      "estimate": {
        "estimate": "string",
        "type": "string"
      },
      "estimateReset": {},
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "memberships": [
        {
          "costRate": {},
          "hourlyRate": {},
          "membershipStatus": "string",
          "membershipType": "string",
          "targetId": "string",
          "userId": "string"
        }
      ],
      "name": "Ava Chen",
      "note": "string",
      "public": true,
      "template": true,
      "timeEstimate": {
        "active": true,
        "estimate": "string",
        "includeNonBillable": true,
        "resetOption": {},
        "type": "string"
      },
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billable` | boolean |  |
| `budgetEstimate` | object |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `color` | string |  |
| `costRate` | object |  |
| `duration` | string |  |
| `estimate.estimate` | string |  |
| `estimate.type` | string |  |
| `estimateReset` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `memberships[].costRate` | object |  |
| `memberships[].hourlyRate` | object |  |
| `memberships[].membershipStatus` | string |  |
| `memberships[].membershipType` | string |  |
| `memberships[].targetId` | string |  |
| `memberships[].userId` | string |  |
| `name` | string |  |
| `note` | string |  |
| `public` | boolean |  |
| `template` | boolean |  |
| `timeEstimate.active` | boolean |  |
| `timeEstimate.estimate` | string |  |
| `timeEstimate.includeNonBillable` | boolean |  |
| `timeEstimate.resetOption` | object |  |
| `timeEstimate.type` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/projects` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-projects.md) for the provider-specific parameters and requirements.

