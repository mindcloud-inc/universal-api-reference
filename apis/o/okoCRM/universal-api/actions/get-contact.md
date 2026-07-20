# OkoCRM: Get contact

Retrieves contact details from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-contact?${params}`, {
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
| `contact_id` | number | yes | The OkoCRM contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_id": 1,
      "avatar_url": "https://example.com",
      "city_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_born": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "id": 1,
      "initials": "string",
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "source_id": 1,
      "tabs": [
        {}
      ],
      "tags": [
        {}
      ],
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
| `avatar_url` | string |  |
| `city_id` | number |  |
| `created_at` | date |  |
| `date_born` | date |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `initials` | string |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `source_id` | number |  |
| `tabs` | array<object> |  |
| `tags` | array<object> |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /contacts/[:contact_id]/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

