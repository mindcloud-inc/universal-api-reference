# Splitwise: List Expenses

Retrieves the current user's expenses from Splitwise.

```
GET https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/list-expenses?${params}`, {
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
| `datedAfter` | date | no | Only return expenses dated after this timestamp. |
| `datedBefore` | date | no | Only return expenses dated before this timestamp. |
| `friendId` | number | no | Only return expenses involving this Splitwise user. |
| `groupId` | number | no | Only return expenses in this Splitwise group. |
| `limit` | number | no | Maximum number of expenses to return. |
| `offset` | number | no | Number of expenses to skip before returning results. |
| `updatedAfter` | date | no | Only return expenses updated after this timestamp. |
| `updatedBefore` | date | no | Only return expenses updated before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {},
      "expenses": [
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
| `errors` | object | Provider-side expense query errors when present. |
| `expenses` | array<object> | Expenses visible to the current user. |

## Native endpoint

Through the native Splitwise API, this operation is `GET /get_expenses` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

