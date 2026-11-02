# BambooHR: List Employee Time Off Policies V1 1

Lists employee time off policies v1 1 from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employee-time-off-policies-v11
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employee-time-off-policies-v11?connectionId=$CONNECTION_ID&employeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employee-time-off-policies-v11?${params}`, {
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
| `employeeId` | string | yes | The internal employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accrualStartDate": "string",
      "timeOffPolicyId": "string",
      "timeOffTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accrualStartDate` | string |  |
| `timeOffPolicyId` | string |  |
| `timeOffTypeId` | number |  |

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1_1/employees/:employeeId/time_off/policies` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-time-off-policies-v11.md) for the provider-specific parameters and requirements.

