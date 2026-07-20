# Planday: Get Shift

Retrieves an existing shift from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-shift?connectionId=$CONNECTION_ID&shiftId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shiftId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-shift?${params}`, {
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
| `shiftId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "dateTimeCreated": "2026-05-07T12:00:00.000Z",
      "dateTimeModified": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "employeeGroupId": 1,
      "employeeId": 1,
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "positionId": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `dateTimeCreated` | date |  |
| `dateTimeModified` | date |  |
| `departmentId` | number |  |
| `employeeGroupId` | number |  |
| `employeeId` | number |  |
| `endDateTime` | date |  |
| `id` | number |  |
| `positionId` | number |  |
| `startDateTime` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /scheduling/v1.0/shifts/:shiftId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shift.md) for the provider-specific parameters and requirements.

