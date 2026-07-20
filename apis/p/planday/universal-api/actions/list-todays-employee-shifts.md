# Planday: List Today's Employee Shifts

Retrieves today's employee shifts from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-todays-employee-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-todays-employee-shifts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-todays-employee-shifts?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "shiftId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shiftId` | number |  |

## Native endpoint

Through the native Planday API, this operation is `GET /punchclock/v1.0/employeeshifts/today` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-todays-employee-shifts.md) for the provider-specific parameters and requirements.

