# RotaCloud: Get Attendance Record

Retrieves an attendance record from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-attendance-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-attendance-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-attendance-record?${params}`, {
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
| `id` | number | yes | The attendance record identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "deleted": true,
      "hours": 1,
      "id": 1,
      "in_location": {},
      "in_time": 1,
      "location": 1,
      "minutes_break": 1,
      "notes": "string",
      "out_location": {},
      "out_time": 1,
      "role": 1,
      "shift": {},
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `deleted` | boolean |  |
| `hours` | number |  |
| `id` | number |  |
| `in_location` | object |  |
| `in_time` | number |  |
| `location` | number |  |
| `minutes_break` | number |  |
| `notes` | string |  |
| `out_location` | object |  |
| `out_time` | number |  |
| `role` | number |  |
| `shift` | object |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/attendance/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendance-record.md) for the provider-specific parameters and requirements.

