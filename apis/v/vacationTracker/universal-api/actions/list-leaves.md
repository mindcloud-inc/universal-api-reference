# Vacation Tracker: List Leaves



```
GET https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-leaves
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vacation Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-leaves?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-04-01&endDate=2026-04-30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-04-01",
  "endDate": "2026-04-30"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-leaves?${params}`, {
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
| `startDate` | string | yes | Date in YYYY-MM-DD format. Example: `2026-04-01`. |
| `endDate` | string | yes | Date in YYYY-MM-DD format. Cannot be before the start date. Example: `2026-04-30`. |
| `status` | list<string> | no | Leave request status. Defaults to APPROVED. One of: `APPROVED`, `CANCELLED`, `DELETED`, `DENIED`, `EXPIRED`, `OPEN`. Default: `APPROVED`. Example: `APPROVED`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand` | list<string> | no | Related leave request object to expand. One of: `approver`, `leaveType`, `user`. Example: `leaveType`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approver": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "departmentId": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "endHour": 1,
      "endMinute": 1,
      "id": "string",
      "isFullDayLeave": true,
      "leaveType": {
        "id": "string",
        "name": "Ava Chen"
      },
      "leaveTypeId": "string",
      "locationId": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "startHour": 1,
      "startMinute": 1,
      "status": "string",
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approver.email` | string | Expanded approver email address. |
| `approver.id` | string | Expanded approver user ID. |
| `approver.name` | string | Expanded approver name. |
| `createdAt` | date | Creation timestamp. |
| `departmentId` | string | Department ID at the time the leave request was sent. |
| `endDate` | date | Leave end date. |
| `endHour` | number | Leave end hour when applicable. |
| `endMinute` | number | Leave end minute when applicable. |
| `id` | string | Leave request ID. |
| `isFullDayLeave` | boolean | Whether the leave is a full-day leave. |
| `leaveType.id` | string | Expanded leave type ID. |
| `leaveType.name` | string | Expanded leave type name. |
| `leaveTypeId` | string | Leave type ID. |
| `locationId` | string | Location ID at the time the leave request was sent. |
| `startDate` | date | Leave start date. |
| `startHour` | number | Leave start hour when applicable. |
| `startMinute` | number | Leave start minute when applicable. |
| `status` | string | Leave request status. |
| `user.email` | string | Expanded user email address. |
| `user.id` | string | Expanded user ID. |
| `user.name` | string | Expanded user name. |
| `userId` | string | User ID. |

## Native endpoint

Through the native Vacation Tracker API, this operation is `GET /leaves` (base URL `https://api.vacationtracker.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leaves.md) for the provider-specific parameters and requirements.

