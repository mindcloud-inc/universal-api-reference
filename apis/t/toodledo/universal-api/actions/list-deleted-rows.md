# Toodledo: List Deleted Rows

Retrieves deleted rows from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-rows?connectionId=$CONNECTION_ID&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-rows?${params}`, {
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
| `list` | string | yes | Hexadecimal list ID whose deleted rows should be fetched. |
| `after` | number | no | Return only rows deleted after this GMT Unix timestamp. |

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
| `id` | string | Deleted row ID. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /rows/deleted.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-rows.md) for the provider-specific parameters and requirements.

