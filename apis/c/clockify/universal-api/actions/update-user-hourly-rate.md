# Clockify: Update User Hourly Rate

Updates a user hourly rate in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-hourly-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-hourly-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "amount": "100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-user-hourly-rate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "amount": "100"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `amount` | number | yes | Example: `100`. |
| `since` | string | no | Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cakeOrganizationId": "string",
      "costRate": {
        "amount": 1,
        "currency": "string"
      },
      "currencies": [
        [
          {}
        ]
      ],
      "features": "string",
      "featureSubscriptionType": "string",
      "hourlyRate": {
        "amount": 1,
        "currency": "https://example.com"
      },
      "id": "string",
      "imageUrl": "https://example.com",
      "memberships": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "subdomain": {
        "enabled": true,
        "name": "Ava Chen"
      },
      "workspaceSettings": {
        "activeBillableHours": true,
        "adminOnlyPages": "string",
        "automaticLock": {
          "changeDay": "string",
          "dayOfMonth": 1,
          "firstDay": "string",
          "olderThanPeriod": "string",
          "olderThanValue": 1,
          "type": "string"
        },
        "canSeeTimeSheet": true,
        "canSeeTracker": true,
        "currencyFormat": "string",
        "defaultBillableProjects": true,
        "durationFormat": "string",
        "entityCreationPermissions": {
          "whoCanCreateProjectsAndClients": "string",
          "whoCanCreateTags": "string",
          "whoCanCreateTasks": "string"
        },
        "forceDescription": true,
        "forceProjects": true,
        "forceTags": true,
        "forceTasks": true,
        "isProjectPublicByDefault": true,
        "lockTimeEntries": "string",
        "lockTimeZone": "string",
        "multiFactorEnabled": true,
        "numberFormat": "string",
        "onlyAdminsCanChangeBillableStatus": true,
        "onlyAdminsCreateProject": true,
        "onlyAdminsCreateTag": true,
        "onlyAdminsCreateTask": true,
        "onlyAdminsSeeAllTimeEntries": true,
        "onlyAdminsSeeBillableRates": true,
        "onlyAdminsSeeDashboard": true,
        "onlyAdminsSeePublicProjectsEntries": true,
        "projectFavorites": true,
        "projectGroupingLabel": "string",
        "projectLabel": "string",
        "projectPickerSpecialFilter": true,
        "round": {
          "minutes": "string",
          "round": "string"
        },
        "taskLabel": "string",
        "timeRoundingInReports": true,
        "timeTrackingMode": "string",
        "trackTimeDownToSecond": true,
        "workingDays": [
          [
            "string"
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cakeOrganizationId` | string |  |
| `costRate` | object |  |
| `costRate.amount` | number |  |
| `costRate.currency` | string |  |
| `currencies[]` | array<object> |  |
| `currencies[].code` | string |  |
| `currencies[].id` | string |  |
| `currencies[].isDefault` | boolean |  |
| `features` | string |  |
| `featureSubscriptionType` | string |  |
| `hourlyRate` | object |  |
| `hourlyRate.amount` | number |  |
| `hourlyRate.currency` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `memberships[]` | array<object> |  |
| `memberships[].costRate` | object |  |
| `memberships[].costRate.amount` | number |  |
| `memberships[].costRate.currency` | string |  |
| `memberships[].hourlyRate` | object |  |
| `memberships[].hourlyRate.amount` | number |  |
| `memberships[].hourlyRate.currency` | string |  |
| `memberships[].membershipStatus` | string |  |
| `memberships[].membershipType` | string |  |
| `memberships[].targetId` | string |  |
| `memberships[].userId` | string |  |
| `name` | string |  |
| `subdomain` | object |  |
| `subdomain.enabled` | boolean |  |
| `subdomain.name` | string |  |
| `workspaceSettings` | object |  |
| `workspaceSettings.activeBillableHours` | boolean |  |
| `workspaceSettings.adminOnlyPages` | string |  |
| `workspaceSettings.automaticLock` | object |  |
| `workspaceSettings.automaticLock.changeDay` | string |  |
| `workspaceSettings.automaticLock.dayOfMonth` | number |  |
| `workspaceSettings.automaticLock.firstDay` | string |  |
| `workspaceSettings.automaticLock.olderThanPeriod` | string |  |
| `workspaceSettings.automaticLock.olderThanValue` | number |  |
| `workspaceSettings.automaticLock.type` | string |  |
| `workspaceSettings.canSeeTimeSheet` | boolean |  |
| `workspaceSettings.canSeeTracker` | boolean |  |
| `workspaceSettings.currencyFormat` | string |  |
| `workspaceSettings.defaultBillableProjects` | boolean |  |
| `workspaceSettings.durationFormat` | string |  |
| `workspaceSettings.entityCreationPermissions` | object |  |
| `workspaceSettings.entityCreationPermissions.whoCanCreateProjectsAndClients` | string |  |
| `workspaceSettings.entityCreationPermissions.whoCanCreateTags` | string |  |
| `workspaceSettings.entityCreationPermissions.whoCanCreateTasks` | string |  |
| `workspaceSettings.forceDescription` | boolean |  |
| `workspaceSettings.forceProjects` | boolean |  |
| `workspaceSettings.forceTags` | boolean |  |
| `workspaceSettings.forceTasks` | boolean |  |
| `workspaceSettings.isProjectPublicByDefault` | boolean |  |
| `workspaceSettings.lockTimeEntries` | string |  |
| `workspaceSettings.lockTimeZone` | string |  |
| `workspaceSettings.multiFactorEnabled` | boolean |  |
| `workspaceSettings.numberFormat` | string |  |
| `workspaceSettings.onlyAdminsCanChangeBillableStatus` | boolean |  |
| `workspaceSettings.onlyAdminsCreateProject` | boolean |  |
| `workspaceSettings.onlyAdminsCreateTag` | boolean |  |
| `workspaceSettings.onlyAdminsCreateTask` | boolean |  |
| `workspaceSettings.onlyAdminsSeeAllTimeEntries` | boolean |  |
| `workspaceSettings.onlyAdminsSeeBillableRates` | boolean |  |
| `workspaceSettings.onlyAdminsSeeDashboard` | boolean |  |
| `workspaceSettings.onlyAdminsSeePublicProjectsEntries` | boolean |  |
| `workspaceSettings.projectFavorites` | boolean |  |
| `workspaceSettings.projectGroupingLabel` | string |  |
| `workspaceSettings.projectLabel` | string |  |
| `workspaceSettings.projectPickerSpecialFilter` | boolean |  |
| `workspaceSettings.round` | object |  |
| `workspaceSettings.round.minutes` | string |  |
| `workspaceSettings.round.round` | string |  |
| `workspaceSettings.taskLabel` | string |  |
| `workspaceSettings.timeRoundingInReports` | boolean |  |
| `workspaceSettings.timeTrackingMode` | string |  |
| `workspaceSettings.trackTimeDownToSecond` | boolean |  |
| `workspaceSettings.workingDays[]` | array<string> |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/users/:userId/hourly-rate` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-hourly-rate.md) for the provider-specific parameters and requirements.

