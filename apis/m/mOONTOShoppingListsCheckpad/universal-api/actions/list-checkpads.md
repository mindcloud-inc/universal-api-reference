# MOONTO Shopping Lists - Checkpad: List Checkpads

Retrieves a list of checkpads from Checkpad.

```
GET https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-checkpads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOONTO Shopping Lists - Checkpad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-checkpads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOONTOShoppingListsCheckpad/latest/actions/list-checkpads?${params}`, {
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

Through the native MOONTO Shopping Lists - Checkpad API, this operation is `GET /checkpads/` (base URL `https://api.moonto.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkpads.md) for the provider-specific parameters and requirements.

