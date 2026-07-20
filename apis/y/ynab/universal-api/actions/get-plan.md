# YNAB: Get Plan

Retrieves a full plan export from YNAB.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-plan?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-plan?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used. |
| `lastKnowledgeOfServer` | number | no | Only include entities changed since this server knowledge value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "categories": [
        {}
      ],
      "categoryGroups": [
        {}
      ],
      "currencyFormat": {},
      "dateFormat": {},
      "firstMonth": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastModifiedOn": "2026-05-07T12:00:00.000Z",
      "lastMonth": "2026-05-07T12:00:00.000Z",
      "months": [
        {}
      ],
      "name": "Ava Chen",
      "payeeLocations": [
        {}
      ],
      "payees": [
        {}
      ],
      "scheduledSubtransactions": [
        {}
      ],
      "scheduledTransactions": [
        {}
      ],
      "subtransactions": [
        {}
      ],
      "transactions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | The accounts in the plan. |
| `categories` | array<object> | The categories in the plan. |
| `categoryGroups` | array<object> | The category groups in the plan. |
| `currencyFormat` | object | The plan currency format settings. |
| `dateFormat` | object | The plan date format settings. |
| `firstMonth` | date | The first month available in the plan. |
| `id` | string | The YNAB plan ID. |
| `lastModifiedOn` | date | When the plan was last modified. |
| `lastMonth` | date | The last month available in the plan. |
| `months` | array<object> | The months in the plan. |
| `name` | string | The plan name. |
| `payeeLocations` | array<object> | The payee locations in the plan. |
| `payees` | array<object> | The payees in the plan. |
| `scheduledSubtransactions` | array<object> | The scheduled subtransactions in the plan. |
| `scheduledTransactions` | array<object> | The scheduled transactions in the plan. |
| `subtransactions` | array<object> | The subtransactions in the plan. |
| `transactions` | array<object> | The transactions in the plan. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

