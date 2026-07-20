# Classe365: Get Attendance by Date (Linear View)

Retrieves attendance data in linear view from Classe365.

```
GET https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-attendance-by-date-linear-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-attendance-by-date-linear-view?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classe365/latest/actions/get-attendance-by-date-linear-view?${params}`, {
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
| `acds_id` | string | no | Academic session id. |
| `date` | string | no | Attendance date in YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "studentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `date` | date |  |
| `status` | string |  |
| `studentId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `GET /rest/attendanceByDateInLV` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendance-by-date-linear-view.md) for the provider-specific parameters and requirements.

