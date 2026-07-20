# MyHR: Activate Employee



```
PUT https://connect.mindcloud.co/v1/universal/myHR/latest/actions/activate-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/activate-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateEffective": "string",
  "employeePid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/activate-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateEffective": "string",
    "employeePid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Optional activation comment. |
| `dateEffective` | string | yes | The activation effective date in YYYY-MM-DD format. |
| `employeePid` | string | yes | The employee PID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "dateCreation": "string",
      "dateEffective": "string",
      "dateLastAction": "string",
      "object": "string",
      "pid": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `dateCreation` | string |  |
| `dateEffective` | string |  |
| `dateLastAction` | string |  |
| `object` | string |  |
| `pid` | number |  |
| `status` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `POST /hr/employees/:employee_pid/statuses/do/activate` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-employee.md) for the provider-specific parameters and requirements.

