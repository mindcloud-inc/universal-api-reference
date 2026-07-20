# Toodledo: List Deleted Lists

Retrieves deleted lists from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-lists?${params}`, {
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
| `after` | number | no | Return only lists deleted after this GMT Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | number | Deletion timestamp. |
| `id` | string | Deleted list ID. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /lists/deleted.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-lists.md) for the provider-specific parameters and requirements.

