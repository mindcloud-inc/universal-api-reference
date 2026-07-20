# MOONTO Shopping Lists - Checkpad: Delete List Item

Deletes a shopping list item from Checkpad.

```
DELETE https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/delete-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/delete-list-item?connectionId=$CONNECTION_ID&list_id=string&item=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string",
  "item": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/delete-list-item?${params}`, {
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
| `list_id` | string | yes | The ID of the MOONTO list containing the item. |
| `item` | string | yes | The item name to delete from the list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOONTO Shopping Lists - Checkpad API returns.

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `DELETE /lists/{list_id}/delete` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list-item.md) for the provider-specific parameters and requirements.

