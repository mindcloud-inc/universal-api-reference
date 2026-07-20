# MOONTO Shopping Lists - Checkpad: Check List Item

Marks a shopping list item as done in Checkpad.

```
PUT https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/check-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/check-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "item": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/check-list-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "item": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | string | yes | The ID of the MOONTO list containing the item. |
| `item` | string | yes | The item name to mark as done. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOONTO Shopping Lists - Checkpad API returns.

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `PUT /lists/{list_id}/check` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-list-item.md) for the provider-specific parameters and requirements.

