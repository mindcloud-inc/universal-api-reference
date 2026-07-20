# Clockify: List Expense Categories

Lists all expense categories in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-expense-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-expense-categories?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-expense-categories?${params}`, {
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
| `workspaceId` | list<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | no | Example: `true`. |
| `name` | string | no | Example: `Example Name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        [
          {}
        ]
      ],
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | array<object> |  |
| `categories[].archived` | boolean |  |
| `categories[].hasUnitPrice` | boolean |  |
| `categories[].id` | string |  |
| `categories[].name` | string |  |
| `categories[].priceInCents` | number |  |
| `categories[].unit` | string |  |
| `categories[].workspaceId` | string |  |
| `count` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/expenses/categories` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expense-categories.md) for the provider-specific parameters and requirements.

