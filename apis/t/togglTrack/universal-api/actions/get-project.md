# Toggl Track: Get Project

Retrieves a project from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-project?connectionId=$CONNECTION_ID&workspaceId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-project?${params}`, {
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
| `workspaceId` | number | yes |  |
| `projectId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "actualHours": {},
      "actualSeconds": {},
      "at": "string",
      "autoEstimates": true,
      "billable": true,
      "canTrackTime": true,
      "cid": {},
      "clientId": {},
      "clientName": {},
      "color": "string",
      "createdAt": "string",
      "currency": {},
      "estimatedHours": {},
      "estimatedSeconds": {},
      "fixedFee": {},
      "id": 1,
      "isPrivate": true,
      "name": "Ava Chen",
      "rate": {},
      "rateLastUpdated": {},
      "recurring": true,
      "recurringParameters": {},
      "serverDeletedAt": {},
      "startDate": "string",
      "status": "string",
      "template": true,
      "templateId": {},
      "totalCount": 1,
      "wid": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `actualHours` | object |  |
| `actualSeconds` | object |  |
| `at` | string |  |
| `autoEstimates` | boolean |  |
| `billable` | boolean |  |
| `canTrackTime` | boolean |  |
| `cid` | object |  |
| `clientId` | object |  |
| `clientName` | object |  |
| `color` | string |  |
| `createdAt` | string |  |
| `currency` | object |  |
| `estimatedHours` | object |  |
| `estimatedSeconds` | object |  |
| `fixedFee` | object |  |
| `id` | number |  |
| `isPrivate` | boolean |  |
| `name` | string |  |
| `rate` | object |  |
| `rateLastUpdated` | object |  |
| `recurring` | boolean |  |
| `recurringParameters` | object |  |
| `serverDeletedAt` | object |  |
| `startDate` | string |  |
| `status` | string |  |
| `template` | boolean |  |
| `templateId` | object |  |
| `totalCount` | number |  |
| `wid` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces/:workspace_id/projects/:project_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

