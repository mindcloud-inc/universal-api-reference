# QDS: Get Employee

Retrieves an employee from QDS by ID.

```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-employee?connectionId=$CONNECTION_ID&employeeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-employee?${params}`, {
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
| `employeeId` | number | yes | The QDS employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employee": {
        "can_log_in": true,
        "can_view_all": true,
        "cell": "string",
        "email": "ava@example.com",
        "email_status": "ava@example.com",
        "id": 1,
        "image_url": "https://example.com",
        "name": "Ava Chen",
        "pid": "string",
        "sms_status": "string",
        "start_date": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "survey_name": "Ava Chen",
        "terminated_reason": "string",
        "termination_date": "2026-05-07T12:00:00.000Z",
        "weekly_report": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employee.can_log_in` | boolean |  |
| `employee.can_view_all` | boolean |  |
| `employee.cell` | string |  |
| `employee.email` | string |  |
| `employee.email_status` | string |  |
| `employee.id` | number |  |
| `employee.image_url` | string |  |
| `employee.name` | string |  |
| `employee.pid` | string |  |
| `employee.sms_status` | string |  |
| `employee.start_date` | date |  |
| `employee.status` | string |  |
| `employee.survey_name` | string |  |
| `employee.terminated_reason` | string |  |
| `employee.termination_date` | date |  |
| `employee.weekly_report` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /employees/:employeeId` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

