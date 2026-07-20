# HoorayHR: Get Leave Type

Retrieves a leave type from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-leave-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-leave-type?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-leave-type?${params}`, {
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
| `id` | number | yes | The leave type ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accumulateBudgetWhenAbsent": 1,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "autoApproveLimit": 1,
      "budget": 1,
      "calculationMethod": "string",
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": 1,
      "icon": "string",
      "id": 1,
      "invisibleInCalendar": 1,
      "isDemoData": 1,
      "isLegacy": 1,
      "leaveInDays": 1,
      "leaveTypeRules": [
        {}
      ],
      "leaveTypeSystemCategory": "string",
      "name": "Ava Chen",
      "periodOffset": 1,
      "preventNegativeBudgetOnRequest": 1,
      "returnLeaveWhileSick": 1,
      "sendExpirationNotifications": 1,
      "subtractHolidays": 1,
      "unpaidLeave": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "useLeaveBudgetOnHoliday": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accumulateBudgetWhenAbsent` | number |  |
| `archivedAt` | date |  |
| `autoApproveLimit` | number |  |
| `budget` | number |  |
| `calculationMethod` | string |  |
| `color` | string |  |
| `createdAt` | date |  |
| `default` | number |  |
| `icon` | string |  |
| `id` | number |  |
| `invisibleInCalendar` | number |  |
| `isDemoData` | number |  |
| `isLegacy` | number |  |
| `leaveInDays` | number |  |
| `leaveTypeRules` | array<object> |  |
| `leaveTypeSystemCategory` | string |  |
| `name` | string |  |
| `periodOffset` | number |  |
| `preventNegativeBudgetOnRequest` | number |  |
| `returnLeaveWhileSick` | number |  |
| `sendExpirationNotifications` | number |  |
| `subtractHolidays` | number |  |
| `unpaidLeave` | number |  |
| `updatedAt` | date |  |
| `useLeaveBudgetOnHoliday` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /leave-types/:id` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-type.md) for the provider-specific parameters and requirements.

