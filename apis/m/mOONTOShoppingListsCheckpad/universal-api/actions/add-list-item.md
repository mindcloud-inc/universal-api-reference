# MOONTO Shopping Lists - Checkpad: Add List Item

Creates a new shopping list item in Checkpad.

```
POST https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/add-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/add-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "item": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/add-list-item', {
  method: 'POST',
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
| `list_id` | string | yes | The ID of the MOONTO list that will receive the item. |
| `item` | string | yes | The item name to add to the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category_id": "string",
      "description": "string",
      "done": true,
      "id_item": "string",
      "image_url": "https://example.com",
      "name": "Ava Chen",
      "price": 1,
      "quantity": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category_id` | string |  |
| `description` | string |  |
| `done` | boolean |  |
| `id_item` | string |  |
| `image_url` | string |  |
| `name` | string |  |
| `price` | number |  |
| `quantity` | string |  |

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `PUT /lists/{list_id}/add` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-list-item.md) for the provider-specific parameters and requirements.

