# Moxie: Create Time Entry

Creates a new time entry in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timerStart": "2026-05-07T12:00:00.000Z",
  "timerEnd": "2026-05-07T12:00:00.000Z",
  "userEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timerStart": "2026-05-07T12:00:00.000Z",
    "timerEnd": "2026-05-07T12:00:00.000Z",
    "userEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timerStart` | date | yes | Time entry start timestamp. |
| `timerEnd` | date | yes | Time entry end timestamp. |
| `userEmail` | string | yes | Email of the user logging time. |
| `clientName` | string | no | Client name for the time entry. |
| `projectName` | string | no | Project name for the time entry. |
| `deliverableName` | string | no | Deliverable name for the time entry. |
| `notes` | string | no | Notes for the time entry. |
| `createClient` | boolean | no | Create the client if it does not exist. |
| `createProject` | boolean | no | Create the project if it does not exist. |
| `createDeliverable` | boolean | no | Create the deliverable if it does not exist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "billable": true,
      "clientId": "string",
      "clientName": "Ava Chen",
      "duration": 1,
      "format": "string",
      "id": "string",
      "notes": "string",
      "pausedAt": "2026-05-07T12:00:00.000Z",
      "pausedSeconds": 1,
      "projectId": "string",
      "projectName": "Ava Chen",
      "sampleData": true,
      "timerEnd": "2026-05-07T12:00:00.000Z",
      "timerStart": "2026-05-07T12:00:00.000Z",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userFullName": "Ava Chen",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `billable` | boolean |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `duration` | number |  |
| `format` | string |  |
| `id` | string |  |
| `notes` | string |  |
| `pausedAt` | date |  |
| `pausedSeconds` | number |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `sampleData` | boolean |  |
| `timerEnd` | date |  |
| `timerStart` | date |  |
| `timestamp` | date |  |
| `userFullName` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/timeWorked/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

