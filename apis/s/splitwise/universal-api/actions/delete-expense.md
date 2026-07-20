# Splitwise: Delete Expense

Deletes an existing expense from Splitwise.

```
DELETE https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-expense?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-expense?${params}`, {
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
| `id` | number | yes | Splitwise expense ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the expense deletion succeeded. |

## Native endpoint

Through the native Splitwise API, this operation is `POST /delete_expense/[:id]` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-expense.md) for the provider-specific parameters and requirements.

