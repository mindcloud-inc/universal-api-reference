# FreshBooks: Get Time Entry

Retrieves a time entry from FreshBooks for a business.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&businessId=string&timeEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string",
  "timeEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-time-entry?${params}`, {
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
| `businessId` | string | yes | FreshBooks business ID. |
| `timeEntryId` | string | yes | FreshBooks time entry ID. |

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

Through the native FreshBooks API, this operation is `GET /timetracking/business/:businessId/time_entries/:timeEntryId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

