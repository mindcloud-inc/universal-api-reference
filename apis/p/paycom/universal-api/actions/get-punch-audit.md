# Paycom: Get Punch Audit

The Get method returns historical information for an employee's punches in a given date range. This method defaults to the current pay period of the employee. Date range may not exceed 30 days.

```
GET https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-punch-audit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-punch-audit?connectionId=$CONNECTION_ID&eecode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eecode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/get-punch-audit?${params}`, {
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
| `audittype` | list | no |  |
| `eecode` | string | yes |  |
| `startdate` | date | no | This is the start date of the request in UNIX format. |
| `enddate` | date | no | This is the end date of the request in UNIX format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "errorCount": 1,
      "errors": [
        "string"
      ],
      "records": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `errorCount` | number |  |
| `errors[]` | string |  |
| `records` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Paycom API, this operation is `GET api/v1/employee/:eecode/punchaudit` (base URL `https://api.paycomonline.net/v4/rest/index.php/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-punch-audit.md) for the provider-specific parameters and requirements.

