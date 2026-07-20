# MyHR: List Employee Addresses



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-addresses?connectionId=$CONNECTION_ID&employeePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employee-addresses?${params}`, {
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
      "city": "string",
      "comment": {},
      "complements": {},
      "countryCode": "string",
      "dateCreation": "string",
      "dateEffective": "string",
      "dateLastAction": "string",
      "isTrashed": "string",
      "number": "string",
      "object": "string",
      "pid": 1,
      "state": {},
      "street": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `comment` | object |  |
| `complements` | object |  |
| `countryCode` | string |  |
| `dateCreation` | string |  |
| `dateEffective` | string |  |
| `dateLastAction` | string |  |
| `isTrashed` | string |  |
| `number` | string |  |
| `object` | string |  |
| `pid` | number |  |
| `state` | object |  |
| `street` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /hr/employees/:employee_pid/addresses` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-addresses.md) for the provider-specific parameters and requirements.

