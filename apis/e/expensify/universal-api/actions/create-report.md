# Expensify: Create Report

Creates a new report in Expensify.

```
POST https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string",
  "employeeEmail": "ava@example.com",
  "reportTitle": "string",
  "expensesJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/create-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "string",
    "employeeEmail": "ava@example.com",
    "reportTitle": "string",
    "expensesJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | The policy to create the report in. |
| `employeeEmail` | string | yes | The account that should own the created report. |
| `reportTitle` | string | yes | The title of the report to create. |
| `expensesJson` | string | yes | JSON array of expense objects to create on the report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reportID": "string",
      "reportName": "Ava Chen",
      "responseCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reportID` | string |  |
| `reportName` | string |  |
| `responseCode` | number |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-report.md) for the provider-specific parameters and requirements.

