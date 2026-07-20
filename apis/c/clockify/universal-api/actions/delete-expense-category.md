# Clockify: Delete Expense Category

Deletes an existing expense category from Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-expense-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-expense-category?connectionId=$CONNECTION_ID&workspaceId=string&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-expense-category?${params}`, {
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
| `categoryId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string | The identifier of the deleted expense category. |

## Native endpoint

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/expenses/categories/:categoryId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-expense-category.md) for the provider-specific parameters and requirements.

