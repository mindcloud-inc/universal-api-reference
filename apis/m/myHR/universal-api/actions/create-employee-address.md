# MyHR: Create Employee Address



```
POST https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "city": "string",
  "countryCode": "string",
  "dateEffective": "string",
  "employeePid": "string",
  "number": "string",
  "street": "string",
  "zipCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "city": "string",
    "countryCode": "string",
    "dateEffective": "string",
    "employeePid": "string",
    "number": "string",
    "street": "string",
    "zipCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | yes | The city name. |
| `comment` | string | no | Optional comment for the address record. |
| `countryCode` | string | yes | The 2-letter country code. |
| `dateEffective` | string | yes | The date the address becomes effective in YYYY-MM-DD format. |
| `employeePid` | string | yes | The employee PID. |
| `number` | string | yes | The street number. |
| `street` | string | yes | The street name. |
| `zipCode` | string | yes | The ZIP or postal code. |

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
| `number` | string |  |
| `object` | string |  |
| `pid` | number |  |
| `state` | object |  |
| `street` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `POST /hr/employees/:employee_pid/addresses` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee-address.md) for the provider-specific parameters and requirements.

