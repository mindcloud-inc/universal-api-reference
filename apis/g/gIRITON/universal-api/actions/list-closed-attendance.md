# GIRITON: List Closed Attendance

Retrieves closed attendance records for a selected GIRITON month.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-closed-attendance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-closed-attendance?connectionId=$CONNECTION_ID&limit=25&offset=0&period=2026-04" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "period": "2026-04"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-closed-attendance?${params}`, {
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
| `period` | string | yes | Required month of the queried period, for example 2022-01. Example: `2026-04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Closed attendance items. |
| `pagination` | object | Pagination metadata. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /attendance/closedAttendance` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-closed-attendance.md) for the provider-specific parameters and requirements.

