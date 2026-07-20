# LinkAce: Create Note

Creates a new note in LinkAce.

```
POST https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkAce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "deleted_at": "string",
      "id": 1,
      "link_id": 1,
      "note": "string",
      "updated_at": "string",
      "user_id": 1,
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Creation timestamp. |
| `deleted_at` | string | Deletion timestamp when present. |
| `id` | number | Unique note identifier. |
| `link_id` | number | Associated link identifier. |
| `note` | string | Note body. |
| `updated_at` | string | Last update timestamp. |
| `user_id` | number | Owning user identifier. |
| `visibility` | number | Visibility value for the note. |

## Native endpoint

Through the native LinkAce API, this operation is `POST /notes` (base URL `https://demo.linkace.org/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

