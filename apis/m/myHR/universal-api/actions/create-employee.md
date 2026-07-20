# MyHR: Create Employee



```
POST https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hireDate": "string",
  "person.firstName": "Ava",
  "person.language": "string",
  "person.lastName": "Chen",
  "person.workEmail": "ava@example.com",
  "seniorityDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hireDate": "string",
    "person.firstName": "Ava",
    "person.language": "string",
    "person.lastName": "Chen",
    "person.workEmail": "ava@example.com",
    "seniorityDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hireDate` | string | yes | The employee hire date in YYYY-MM-DD format. |
| `internalNumber` | string | no | Optional internal employee number. |
| `person.firstName` | string | yes | The employee first name. |
| `person.language` | string | yes | The employee language. |
| `person.lastName` | string | yes | The employee last name. |
| `person.workEmail` | string | yes | The employee work email. |
| `seniorityDate` | string | yes | The employee seniority date in YYYY-MM-DD format. |

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

Through the native MyHR API, this operation is `POST /employees` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee.md) for the provider-specific parameters and requirements.

