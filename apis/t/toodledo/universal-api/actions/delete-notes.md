# Toodledo: Delete Notes

Deletes existing notes from Toodledo.

```
DELETE https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-notes?connectionId=$CONNECTION_ID&notes=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notes": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-notes?${params}`, {
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
| `notes` | string | yes | JSON-encoded array of note IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Deleted note ID. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /notes/delete.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-notes.md) for the provider-specific parameters and requirements.

