# MyHR: List Employees



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employees?${params}`, {
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
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "employeeStatus": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "object": "string",
        "pid": "string",
        "tag": {}
      },
      "foreignKey": "string",
      "hireDate": "string",
      "internalNumber": "string",
      "object": "string",
      "person": {
        "birthDate": "string",
        "dateCreation": "string",
        "dateLastAction": "string",
        "firstName": "Ava",
        "gender": "string",
        "hasSelfService": true,
        "language": "string",
        "object": "string",
        "phonePersonalMobile": "string",
        "phonePersonalMobileCountryCode": "string",
        "phonePersonalMobileFormatted": "string",
        "pid": "string",
        "usualName": "Ava Chen",
        "workEmail": "ava@example.com"
      },
      "pid": "string",
      "seniorityDate": "string",
      "sosecNumber": "string"
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
| `employeeStatus.dateCreation` | string |  |
| `employeeStatus.dateLastAction` | string |  |
| `employeeStatus.object` | string |  |
| `employeeStatus.pid` | string |  |
| `employeeStatus.tag` | object |  |
| `foreignKey` | string |  |
| `hireDate` | string |  |
| `internalNumber` | string |  |
| `object` | string |  |
| `person.birthDate` | string |  |
| `person.dateCreation` | string |  |
| `person.dateLastAction` | string |  |
| `person.firstName` | string |  |
| `person.gender` | string |  |
| `person.hasSelfService` | boolean |  |
| `person.language` | string |  |
| `person.object` | string |  |
| `person.phonePersonalMobile` | string |  |
| `person.phonePersonalMobileCountryCode` | string |  |
| `person.phonePersonalMobileFormatted` | string |  |
| `person.pid` | string |  |
| `person.usualName` | string |  |
| `person.workEmail` | string |  |
| `pid` | string |  |
| `seniorityDate` | string |  |
| `sosecNumber` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employees` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

