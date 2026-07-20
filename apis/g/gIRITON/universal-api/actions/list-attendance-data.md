# GIRITON: List Attendance Data

Retrieves configured attendance data from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-data?${params}`, {
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
| `dateFrom` | string | no | Beginning of the attendance time period. |
| `dateTo` | string | no | End of the attendance time period. |
| `personIds` | string | no | Comma-separated database IDs of persons. |

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
| `items` | array<object> | Attendance data items. |
| `pagination` | object | Pagination metadata. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /attendance/attendanceData` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-attendance-data.md) for the provider-specific parameters and requirements.

