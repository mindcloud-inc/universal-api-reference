# Splitwise: List Expense Comments

Retrieves comments for an expense in Splitwise.

```
GET https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expense-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expense-comments?connectionId=$CONNECTION_ID&expenseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expenseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expense-comments?${params}`, {
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
| `expenseId` | number | yes | Splitwise expense ID whose comments should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
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
| `comments` | array<object> | Comments for the requested Splitwise expense. |

## Native endpoint

Through the native Splitwise API, this operation is `GET /get_comments` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expense-comments.md) for the provider-specific parameters and requirements.

