# Toggl Track: List Workspaces

Retrieves workspaces from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activeProjectCount": 1,
      "admin": true,
      "apiToken": "string",
      "at": "string",
      "businessWs": true,
      "csvUpload": {},
      "defaultCurrency": "string",
      "defaultHourlyRate": {},
      "disableApprovals": true,
      "disableExpenses": true,
      "disableTimesheetView": true,
      "hideStartEndTimes": true,
      "icalEnabled": true,
      "icalUrl": "https://example.com",
      "id": 1,
      "lastModified": "string",
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
| `activeProjectCount` | number |  |
| `admin` | boolean |  |
| `apiToken` | string |  |
| `at` | string |  |
| `businessWs` | boolean |  |
| `csvUpload` | object |  |
| `defaultCurrency` | string |  |
| `defaultHourlyRate` | object |  |
| `disableApprovals` | boolean |  |
| `disableExpenses` | boolean |  |
| `disableTimesheetView` | boolean |  |
| `hideStartEndTimes` | boolean |  |
| `icalEnabled` | boolean |  |
| `icalUrl` | string |  |
| `id` | number |  |
| `lastModified` | string |  |
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

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

