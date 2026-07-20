# Toodledo: List Deleted Notes

Retrieves deleted notes from Toodledo.

```
GET https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/list-deleted-notes?${params}`, {
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
| `after` | number | no | Return only notes deleted after this GMT Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "stamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Deleted note ID. |
| `stamp` | number | Deletion timestamp. |

## Native endpoint

Through the native Toodledo API, this operation is `GET /notes/deleted.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-notes.md) for the provider-specific parameters and requirements.

