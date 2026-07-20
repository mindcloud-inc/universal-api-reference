# Livestorm: List People Attributes

Retrieves people attributes from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-people-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-people-attributes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-people-attributes?${params}`, {
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
| `sort` | string | no | Sortable Fields: (-)slug, name, placeholder, created_at, updated_at |
| `filter[builtin]` | string | no | Filter PeopleAttributes by builtin |
| `filter[description]` | string | no | Filter PeopleAttributes by description |
| `filter[name]` | string | no | Filter PeopleAttributes by name |
| `filter[placeholder]` | string | no | Filter PeopleAttributes by placeholder |
| `filter[slug]` | string | no | Filter PeopleAttributes by slug |
| `filter[type]` | string | no | Filter PeopleAttributes by type (text, email, avatar, url, consent, unique_select, multiple_select) |
| `filter[userId]` | string | no | Filter PeopleAttributes by user_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "builtin": true,
        "description": "string",
        "name": "Ava Chen",
        "options": [
          [
            {}
          ]
        ],
        "placeholder": "string",
        "slug": "string",
        "type": "string",
        "userId": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.builtin` | boolean |  |
| `attributes.description` | string |  |
| `attributes.name` | string |  |
| `attributes.options[]` | array<object> |  |
| `attributes.options[].label` | string |  |
| `attributes.options[].position` | number |  |
| `attributes.options[].value` | string |  |
| `attributes.placeholder` | string |  |
| `attributes.slug` | string |  |
| `attributes.type` | string |  |
| `attributes.userId` | string |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET people_attributes` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people-attributes.md) for the provider-specific parameters and requirements.

