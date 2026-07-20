# YNAB: Get Account

Retrieves an account from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-account?connectionId=$CONNECTION_ID&planId=string&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-account?${params}`, {
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
| `planId` | string | yes |  |
| `accountId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "balanceFormatted": "string",
      "closed": true,
      "deleted": true,
      "id": "string",
      "name": "Ava Chen",
      "onBudget": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | The current account balance in milliunits. |
| `balanceFormatted` | string | The current account balance formatted for display. |
| `closed` | boolean | Whether the account is closed. |
| `deleted` | boolean | Whether the account has been deleted. |
| `id` | string | The YNAB account ID. |
| `name` | string | The account name. |
| `onBudget` | boolean | Whether the account is on budget. |
| `type` | string | The account type. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/accounts/:accountId` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

