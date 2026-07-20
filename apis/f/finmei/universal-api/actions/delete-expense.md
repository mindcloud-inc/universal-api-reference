# Finmei: Delete Expense



```
DELETE https://connect.mindcloud.co/v1/universal/finmei/latest/actions/delete-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/delete-expense?connectionId=$CONNECTION_ID&expenseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expenseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/delete-expense?${params}`, {
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
| `expenseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |

## Native endpoint

Through the native Finmei API, this operation is `DELETE /expenses/:expenseId` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-expense.md) for the provider-specific parameters and requirements.

