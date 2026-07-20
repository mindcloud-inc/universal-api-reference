# Sarbacane: List Lists

Retrieves lists from your Sarbacane account.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-lists?${params}`, {
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
      "count": 1,
      "created": "string",
      "edited": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of contacts in the list. |
| `created` | string | List creation timestamp. |
| `edited` | string | Last modification timestamp. |
| `id` | string | Sarbacane list ID. |
| `kind` | string | Sarbacane list kind. |
| `name` | string | List display name. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /lists` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

