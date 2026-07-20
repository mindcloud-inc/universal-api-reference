# Tidely: List Expense Categories



```
GET https://connect.mindcloud.co/v1/universal/tidely/latest/actions/list-expense-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/list-expense-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/list-expense-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "enabledForPlannedTransactions": true,
      "id": 1,
      "name": "Ava Chen",
      "parentId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabledForPlannedTransactions` | boolean | Whether the category can be used for planned transactions. |
| `id` | number | Tidely category ID. |
| `name` | string | Category name. |
| `parentId` | number | Parent category ID when present. |
| `type` | string | Tidely category type. |

## Native endpoint

Through the native Tidely API, this operation is `GET /api/v1/open-api/categories` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expense-categories.md) for the provider-specific parameters and requirements.

