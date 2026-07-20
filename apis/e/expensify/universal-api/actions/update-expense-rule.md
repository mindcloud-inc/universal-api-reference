# Expensify: Update Expense Rule

Updates an existing expense rule in Expensify.

```
PUT https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-expense-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-expense-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "BE9009315B111E6A",
  "employeeEmail": "apps@mindcloud.co",
  "ruleId": "999999",
  "actionsJson": {
    "defaultBillable": false
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/update-expense-rule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "BE9009315B111E6A",
    "employeeEmail": "apps@mindcloud.co",
    "ruleId": "999999",
    "actionsJson": {"defaultBillable":false}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | The policy to update the rule on. Default: `BE9009315B111E6A`. |
| `employeeEmail` | string | yes | The policy member who should receive the expense rule. Default: `apps@mindcloud.co`. |
| `ruleId` | string | yes | The expense rule ID to update. Default: `999999`. |
| `actionsJson` | string | yes | JSON object containing supported rule actions, for example {"tag":"Tag Name"}. Default: `{"defaultBillable":false}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseCode": 1,
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseCode` | number |  |
| `responseMessage` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-expense-rule.md) for the provider-specific parameters and requirements.

