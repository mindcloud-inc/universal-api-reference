# Toggl Track: Get Workspace

Retrieves a workspace from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": true,
      "apiToken": "string",
      "at": "string",
      "businessWs": true,
      "csvUpload": {},
      "defaultCurrency": "string",
      "defaultHourlyRate": {},
      "disableApprovals": true,
      "disableExpenses": {},
      "disableTimesheetView": true,
      "hideStartEndTimes": true,
      "icalEnabled": true,
      "icalUrl": {},
      "id": 1,
      "lastModified": {},
      "limitPublicProjectData": true,
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "onlyAdminsMayCreateProjects": true,
      "onlyAdminsMayCreateTags": true,
      "onlyAdminsSeeTeamDashboard": true,
      "organizationId": 1,
      "premium": true,
      "projectsBillableByDefault": true,
      "projectsEnforceBillable": true,
      "projectsPrivateByDefault": true,
      "rateLastUpdated": {},
      "reportsCollapse": true,
      "role": "string",
      "rounding": 1,
      "roundingMinutes": 1,
      "serverDeletedAt": {},
      "subscription": {},
      "suspendedAt": {},
      "workingHoursInMinutes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean |  |
| `apiToken` | string |  |
| `at` | string |  |
| `businessWs` | boolean |  |
| `csvUpload` | object |  |
| `defaultCurrency` | string |  |
| `defaultHourlyRate` | object |  |
| `disableApprovals` | boolean |  |
| `disableExpenses` | object |  |
| `disableTimesheetView` | boolean |  |
| `hideStartEndTimes` | boolean |  |
| `icalEnabled` | boolean |  |
| `icalUrl` | object |  |
| `id` | number |  |
| `lastModified` | object |  |
| `limitPublicProjectData` | boolean |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `onlyAdminsMayCreateProjects` | boolean |  |
| `onlyAdminsMayCreateTags` | boolean |  |
| `onlyAdminsSeeTeamDashboard` | boolean |  |
| `organizationId` | number |  |
| `premium` | boolean |  |
| `projectsBillableByDefault` | boolean |  |
| `projectsEnforceBillable` | boolean |  |
| `projectsPrivateByDefault` | boolean |  |
| `rateLastUpdated` | object |  |
| `reportsCollapse` | boolean |  |
| `role` | string |  |
| `rounding` | number |  |
| `roundingMinutes` | number |  |
| `serverDeletedAt` | object |  |
| `subscription` | object |  |
| `suspendedAt` | object |  |
| `workingHoursInMinutes` | object |  |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces/:workspace_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

