# STEL Order: List Expense States

Retrieves a list of expense states from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-expense-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-expense-states?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-expense-states?${params}`, {
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
      "color": "string",
      "color-text": "string",
      "deleted": true,
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "path": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `color-text` | string |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |
| `path` | string |  |
| `type` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /expenseStates` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expense-states.md) for the provider-specific parameters and requirements.

