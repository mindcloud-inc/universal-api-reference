# MOONTO Shopping Lists - Checkpad: Get List Details

Retrieves shopping list details from Checkpad.

```
GET https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-list-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-list-details?connectionId=$CONNECTION_ID&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/get-list-details?${params}`, {
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
| `list_id` | string | yes | The ID of the MOONTO list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "list_id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `list_id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `GET /lists/{list_id}` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-details.md) for the provider-specific parameters and requirements.

