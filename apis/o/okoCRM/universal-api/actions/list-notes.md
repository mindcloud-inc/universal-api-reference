# OkoCRM: List notes

Retrieves notes from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-notes?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-notes?${params}`, {
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
| `contact_id` | number | yes | List notes for a contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "text": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_id` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `text` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /notes/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

