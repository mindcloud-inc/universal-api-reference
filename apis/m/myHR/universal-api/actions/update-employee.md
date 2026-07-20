# MyHR: Update Employee



```
PUT https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeePid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeePid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeePid` | string | yes | The employee PID. |
| `internalNumber` | string | no | Updated internal employee number. |
| `person.firstName` | string | no | Updated employee first name. |
| `person.lastName` | string | no | Updated employee last name. |
| `person.workEmail` | string | no | Updated employee work email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "hireDate": "string",
      "internalNumber": "string",
      "object": "string",
      "person": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "firstName": "Ava",
        "hasSelfService": true,
        "language": "string",
        "object": "string",
        "pid": "string",
        "usualName": "Ava Chen",
        "workEmail": "ava@example.com"
      },
      "pid": "string",
      "seniorityDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `hireDate` | string |  |
| `internalNumber` | string |  |
| `object` | string |  |
| `person.dateCreation` | string |  |
| `person.dateLastAction` | string |  |
| `person.dateLastUpdate` | string |  |
| `person.firstName` | string |  |
| `person.hasSelfService` | boolean |  |
| `person.language` | string |  |
| `person.object` | string |  |
| `person.pid` | string |  |
| `person.usualName` | string |  |
| `person.workEmail` | string |  |
| `pid` | string |  |
| `seniorityDate` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `PUT /employees/:employee_pid` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee.md) for the provider-specific parameters and requirements.

