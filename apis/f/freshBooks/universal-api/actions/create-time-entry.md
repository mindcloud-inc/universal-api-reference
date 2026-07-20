# FreshBooks: Create Time Entry

Creates a new time entry in FreshBooks for a business.

```
POST https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "timeEntry.duration": 1,
  "timeEntry.started_at": "string",
  "timeEntry.identity_id": 1,
  "timeEntry.is_logged": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "timeEntry.duration": 1,
    "timeEntry.started_at": "string",
    "timeEntry.identity_id": 1,
    "timeEntry.is_logged": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes | FreshBooks business ID. |
| `timeEntry.duration` | number | yes | Duration in seconds. |
| `timeEntry.started_at` | string | yes | Start timestamp. |
| `timeEntry.identity_id` | number | yes | FreshBooks identity ID. |
| `timeEntry.client_id` | number | no | FreshBooks client ID. |
| `timeEntry.project_id` | number | no | FreshBooks project ID. |
| `timeEntry.is_logged` | boolean | yes | Whether the entry is logged. |
| `timeEntry.note` | string | no | Time entry note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billable": true,
      "billed": true,
      "clientId": 1,
      "createdAt": "string",
      "duration": 1,
      "id": 1,
      "identityId": 1,
      "internal": true,
      "isLogged": true,
      "localStartedAt": "string",
      "localTimezone": "string",
      "note": "string",
      "pendingClient": {},
      "pendingProject": {},
      "pendingTask": {},
      "projectId": 1,
      "retainerId": 1,
      "serviceId": 1,
      "startedAt": "string",
      "taskId": 1,
      "timer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billable` | boolean |  |
| `billed` | boolean |  |
| `clientId` | number |  |
| `createdAt` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `identityId` | number |  |
| `internal` | boolean |  |
| `isLogged` | boolean |  |
| `localStartedAt` | string |  |
| `localTimezone` | string |  |
| `note` | string |  |
| `pendingClient` | object |  |
| `pendingProject` | object |  |
| `pendingTask` | object |  |
| `projectId` | number |  |
| `retainerId` | number |  |
| `serviceId` | number |  |
| `startedAt` | string |  |
| `taskId` | number |  |
| `timer` | object |  |

## Native endpoint

Through the native FreshBooks API, this operation is `POST /timetracking/business/:businessId/time_entries` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

