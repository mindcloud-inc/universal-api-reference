# Paylocity: Create Employee Punch



```
POST https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/create-employee-punch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paylocity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/create-employee-punch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/create-employee-punch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `d[].employeeId` | string | no |  |
| `d[].lastName` | string | no |  |
| `d[].firstName` | string | no |  |
| `d[].date` | string | no |  |
| `d[].time` | string | no |  |
| `d[].recordType` | string | no |  |
| `d[].employeeNote` | string | no |  |
| `d[].supervisorNote` | string | no |  |
| `d[].payLevel` | string | no |  |
| `d[].costCenter1` | string | no |  |
| `d[].costCenter2` | string | no |  |
| `d[].costCenter3` | string | no |  |
| `d[].costCenter4` | string | no |  |
| `d[].costCenter5` | string | no |  |
| `d[].costCenter6` | string | no |  |
| `d[].costCenter7` | string | no |  |
| `d[].costCenter8` | string | no |  |
| `d[].costCenter9` | string | no |  |
| `d[].costCenter10` | string | no |  |
| `d[].costCenter11` | string | no |  |
| `d[].costCenter12` | string | no |  |
| `d[].costCenter13` | string | no |  |
| `d[].costCenter14` | string | no |  |
| `d[].costCenter15` | string | no |  |
| `d[].hoursDollars` | string | no |  |
| `companyId` | string | yes |  |
| `d[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paylocity API returns.

## Native endpoint

Through the native Paylocity API, this operation is `POST apihub/time/v2/companies/:companyId/punchImport` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee-punch.md) for the provider-specific parameters and requirements.

