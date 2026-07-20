# MyHR: List Employee Bonuses For Employee



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-bonuses-for-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-bonuses-for-employee?connectionId=$CONNECTION_ID&employeePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-bonuses-for-employee?${params}`, {
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
| `employeePid` | string | yes | The employee PID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "attributionDate": "string",
      "companyBonusReason": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "label": "string",
        "object": "string",
        "pid": "string"
      },
      "currency": "string",
      "dateCreation": "string",
      "dateLastAction": "string",
      "object": "string",
      "pid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `attributionDate` | string |  |
| `companyBonusReason.dateCreation` | string |  |
| `companyBonusReason.dateLastAction` | string |  |
| `companyBonusReason.label` | string |  |
| `companyBonusReason.object` | string |  |
| `companyBonusReason.pid` | string |  |
| `currency` | string |  |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `object` | string |  |
| `pid` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employees/:employee_pid/employee_bonuses` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-bonuses-for-employee.md) for the provider-specific parameters and requirements.

