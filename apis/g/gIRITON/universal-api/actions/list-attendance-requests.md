# GIRITON: List Attendance Requests

Retrieves a list of attendance requests from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-requests?${params}`, {
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
| `requestStates` | string | no | Comma-separated request states such as new, approved, refused, deleted, or all. |
| `requestTypes` | string | no | Comma-separated request types such as attendance_new, attendance_change, shift, or all. |
| `dateFrom` | string | no | Start date of the request period. |
| `dateTo` | string | no | End date of the request period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of attendance request entries returned. |
| `entries` | array<object> | Attendance request entries returned by GIRITON. |
| `newestTimestamp` | date | Newest timestamp reported by GIRITON for the request list. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /requests/requests` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attendance-requests.md) for the provider-specific parameters and requirements.

