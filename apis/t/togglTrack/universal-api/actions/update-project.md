# Toggl Track: Update Project

Updates an existing project in Toggl Track.

```
PUT https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes |  |
| `projectId` | list<number> | yes |  |
| `name` | string | no |  |
| `active` | boolean | no |  |
| `isPrivate` | boolean | no |  |
| `billable` | boolean | no |  |
| `clientId` | list<number> | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `estimatedHours` | number | no |  |
| `color` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "actualHours": 1,
      "actualSeconds": 1,
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
| `actualHours` | number |  |
| `actualSeconds` | number |  |
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

Through the native Toggl Track API, this operation is `PUT /api/v9/workspaces/:workspace_id/projects/:project_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

