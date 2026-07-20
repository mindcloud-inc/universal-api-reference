# OkoCRM: List contacts

Retrieves contacts from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-contacts?${params}`, {
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
      "author_id": 1,
      "city_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_born": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "source_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_id` | number |  |
| `city_id` | number |  |
| `created_at` | date |  |
| `date_born` | date |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `source_id` | number |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /contacts/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

