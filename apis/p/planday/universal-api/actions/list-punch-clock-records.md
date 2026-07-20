# Planday: List Punch Clock Records

Retrieves punch clock records from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-punch-clock-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-punch-clock-records?connectionId=$CONNECTION_ID&limit=25&offset=0&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-punch-clock-records?${params}`, {
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
| `employeeId` | number | no |  |
| `from` | string | yes |  |
| `limit` | number | no |  |
| `offset` | number | no |  |
| `shiftId` | number | no |  |
| `to` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "isApproved": true,
      "punchClockShiftId": 1,
      "shiftEndDateTime": "2026-05-07T12:00:00.000Z",
      "shiftId": 1,
      "shiftStartDateTime": "2026-05-07T12:00:00.000Z",
      "startDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDateTime` | date |  |
| `isApproved` | boolean |  |
| `punchClockShiftId` | number |  |
| `shiftEndDateTime` | date |  |
| `shiftId` | number |  |
| `shiftStartDateTime` | date |  |
| `startDateTime` | date |  |

## Native endpoint

Through the native Planday API, this operation is `GET /punchclock/v1.0/punchclockshifts` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-punch-clock-records.md) for the provider-specific parameters and requirements.

