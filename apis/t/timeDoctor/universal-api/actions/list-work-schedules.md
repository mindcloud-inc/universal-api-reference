# Time Doctor: List Work Schedules

Retrieves work schedules from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedules?connectionId=$CONNECTION_ID&from=2026-04-01T00%3A00%3A00Z&to=2026-04-30T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-01T00:00:00Z",
  "to": "2026-04-30T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-work-schedules?${params}`, {
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
| `from` | string | yes | Example: `2026-04-01T00:00:00Z`. |
| `to` | string | yes | Example: `2026-04-30T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "leaveType": "string",
      "minimumHours": 1,
      "reason": "string",
      "reviewedAt": "2026-05-07T12:00:00.000Z",
      "reviewerId": "string",
      "reviewerName": "Ava Chen",
      "start": "2026-05-07T12:00:00.000Z",
      "time": 1,
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `end` | date |  |
| `id` | string |  |
| `leaveType` | string |  |
| `minimumHours` | number |  |
| `reason` | string |  |
| `reviewedAt` | date |  |
| `reviewerId` | string |  |
| `reviewerName` | string |  |
| `start` | date |  |
| `time` | number |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/work-schedules` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-schedules.md) for the provider-specific parameters and requirements.

