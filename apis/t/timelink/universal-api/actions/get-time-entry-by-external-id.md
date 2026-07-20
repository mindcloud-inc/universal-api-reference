# Timelink: Get Time Entry by External ID

Finds a time entry in Timelink by external ID.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-time-entry-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-time-entry-by-external-id?connectionId=$CONNECTION_ID&extId=stage3-time-entry-001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extId": "stage3-time-entry-001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-time-entry-by-external-id?${params}`, {
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
| `extId` | string | yes | The external reference ID for the time entry. Example: `stage3-time-entry-001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billedAt": {},
      "clientId": "string",
      "companyId": "string",
      "createdAt": "string",
      "deletedAt": {},
      "description": "string",
      "endedAt": "string",
      "extToolId": "string",
      "id": "string",
      "isInterrupt": true,
      "lastPush": {},
      "paid": true,
      "projectId": {},
      "pushErrors": {},
      "pushState": {},
      "serviceId": {},
      "startedAt": "string",
      "tempId": {},
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billedAt` | object |  |
| `clientId` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `description` | string |  |
| `endedAt` | string |  |
| `extToolId` | string |  |
| `id` | string |  |
| `isInterrupt` | boolean |  |
| `lastPush` | object |  |
| `paid` | boolean |  |
| `projectId` | object |  |
| `pushErrors` | object |  |
| `pushState` | object |  |
| `serviceId` | object |  |
| `startedAt` | string |  |
| `tempId` | object |  |
| `updatedAt` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `GET /timeEntries/ext/:extId` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry-by-external-id.md) for the provider-specific parameters and requirements.

