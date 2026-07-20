# MyHR: Update Employee Address



```
PUT https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeAddressPid": "string",
  "employeePid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeAddressPid": "string",
    "employeePid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no | Updated city name. |
| `countryCode` | string | no | Updated 2-letter country code. |
| `employeeAddressPid` | string | yes | The employee address PID. |
| `employeePid` | string | yes | The employee PID. |
| `number` | string | no | Updated street number. |
| `street` | string | no | Updated street name. |
| `zipCode` | string | no | Updated ZIP or postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "comment": "string",
      "complements": {},
      "countryCode": "string",
      "dateCreation": "string",
      "dateEffective": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
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
| `comment` | string |  |
| `complements` | object |  |
| `countryCode` | string |  |
| `dateCreation` | string |  |
| `dateEffective` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `isTrashed` | string |  |
| `number` | string |  |
| `object` | string |  |
| `pid` | number |  |
| `state` | object |  |
| `street` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `PATCH /hr/employees/:employee_pid/addresses/:employee_address_pid` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee-address.md) for the provider-specific parameters and requirements.

