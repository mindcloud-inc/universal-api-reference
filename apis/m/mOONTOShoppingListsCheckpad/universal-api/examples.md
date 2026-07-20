# MOONTO Shopping Lists - Checkpad Universal API Examples

These examples use the MindCloud API key and MOONTO Shopping Lists - Checkpad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves a list of shopping lists from Checkpad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mOONTOShoppingListsCheckpad/latest/actions/list-lists).

## Add List Item

Creates a new shopping list item in Checkpad.

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

Example response:

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

See the full [Add List Item action reference](actions/add-list-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mOONTOShoppingListsCheckpad/latest/actions/add-list-item).
