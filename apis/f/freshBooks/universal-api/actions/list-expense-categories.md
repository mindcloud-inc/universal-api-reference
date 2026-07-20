# FreshBooks: List Expense Categories

Retrieves expense categories from FreshBooks for an account.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-expense-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-expense-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/list-expense-categories?${params}`, {
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
| `accountId` | string | yes | FreshBooks account ID from the authenticated business context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "categoryid": 1,
      "createdAt": "string",
      "id": 1,
      "isCogs": true,
      "isEditable": true,
      "parentid": 1,
      "transactionPosted": true,
      "updatedAt": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `categoryid` | number |  |
| `createdAt` | string |  |
| `id` | number |  |
| `isCogs` | boolean |  |
| `isEditable` | boolean |  |
| `parentid` | number |  |
| `transactionPosted` | boolean |  |
| `updatedAt` | string |  |
| `visState` | number |  |

## Native endpoint

Through the native FreshBooks API, this operation is `GET /accounting/account/:accountId/expenses/categories` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expense-categories.md) for the provider-specific parameters and requirements.

