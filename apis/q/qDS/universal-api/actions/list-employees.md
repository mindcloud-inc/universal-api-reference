# QDS: List Employees

Retrieves a list of employees from QDS.

```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-employees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "employees": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employees[].can_log_in` | boolean |  |
| `employees[].can_view_all` | boolean |  |
| `employees[].cell` | string |  |
| `employees[].email` | string |  |
| `employees[].email_status` | string |  |
| `employees[].id` | number |  |
| `employees[].image_url` | string |  |
| `employees[].name` | string |  |
| `employees[].pid` | string |  |
| `employees[].sms_status` | string |  |
| `employees[].start_date` | date |  |
| `employees[].status` | string |  |
| `employees[].survey_name` | string |  |
| `employees[].terminated_reason` | string |  |
| `employees[].termination_date` | date |  |
| `employees[].weekly_report` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /employees` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

