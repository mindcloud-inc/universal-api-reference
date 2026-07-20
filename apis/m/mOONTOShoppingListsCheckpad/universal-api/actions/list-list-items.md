# MOONTO Shopping Lists - Checkpad: List List Items

Retrieves shopping list items from Checkpad.

```
GET https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-list-items?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-list-items?${params}`, {
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
| `list_id` | string | yes | The ID of the MOONTO list whose items should be returned. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `data` | array<object> |  |

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `GET /lists/{list_id}/items` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-list-items.md) for the provider-specific parameters and requirements.

