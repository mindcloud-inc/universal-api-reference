# Sage Intacct: Create Budget



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "2019 Annual Plan",
  "description": "string",
  "periodName": "Month Ended January 2019",
  "budgetItems[]": [
    "string"
  ],
  "budgetItems[].accountNo": "string",
  "budgetItems[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "2019 Annual Plan",
    "description": "string",
    "periodName": "Month Ended January 2019",
    "budgetItems[]": ["string"],
    "budgetItems[].accountNo": "string",
    "budgetItems[].amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budgetId` | string | yes | Example: `2019 Annual Plan`. |
| `description` | string | yes |  |
| `defaultBudget` | boolean | no |  |
| `periodName` | string | yes | Example: `Month Ended January 2019`. |
| `locationNo` | string | no |  |
| `departmentNo` | string | no |  |
| `budgetItems[]` | array | yes |  |
| `budgetItems[].accountNo` | string | yes |  |
| `budgetItems[].amount` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetId": "string",
      "response": {},
      "sageRecordNo": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetId` | string |  |
| `response` | object |  |
| `sageRecordNo` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sage Intacct API, this operation is `POST /` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-budget.md) for the provider-specific parameters and requirements.

