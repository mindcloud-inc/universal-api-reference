# Seven: List Contacts

Retrieves contacts from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/list-contacts?${params}`, {
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
| `orderBy` | string | no | The column by which the contacts should be sorted. |
| `orderDirection` | string | no | The direction of the sorting. Can be either asc or desc . |
| `search` | string | no | You can use this parameter to search in all columns in your contacts. |
| `offset` | number | no | The page to be displayed. |
| `limit` | number | no | The number of contacts to be displayed per page. Can be a value between 30 and 500 . |
| `groupId` | number | no | Only display contacts who are members of a specific group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "avatar": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "groups": [
          1
        ],
        "id": 1,
        "initials": {
          "color": "string",
          "initials": "string"
        },
        "properties": {
          "address": "string",
          "birthday": "2026-05-07T12:00:00.000Z",
          "city": "string",
          "email": "ava@example.com",
          "firstname": "Ava",
          "home_number": "string",
          "lastname": "Chen",
          "mobile_number": 1,
          "notes": "string",
          "postal_code": "string"
        },
        "validation": {
          "state": "string",
          "timestamp": "2026-05-07T12:00:00.000Z"
        }
      },
      "pagingMetadata": {
        "count": 1,
        "has_more": true,
        "limit": 1,
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.avatar` | string |  |
| `data.created` | date |  |
| `data.groups` | array<number> |  |
| `data.id` | number |  |
| `data.initials` | object |  |
| `data.initials.color` | string |  |
| `data.initials.initials` | string |  |
| `data.properties` | object |  |
| `data.properties.address` | string |  |
| `data.properties.birthday` | date |  |
| `data.properties.city` | string |  |
| `data.properties.email` | string |  |
| `data.properties.firstname` | string |  |
| `data.properties.home_number` | string |  |
| `data.properties.lastname` | string |  |
| `data.properties.mobile_number` | number |  |
| `data.properties.notes` | string |  |
| `data.properties.postal_code` | string |  |
| `data.validation` | object |  |
| `data.validation.state` | string |  |
| `data.validation.timestamp` | date |  |
| `pagingMetadata` | object |  |
| `pagingMetadata.count` | number |  |
| `pagingMetadata.has_more` | boolean |  |
| `pagingMetadata.limit` | number |  |
| `pagingMetadata.offset` | number |  |
| `pagingMetadata.total` | number |  |

## Native endpoint

Through the native Seven API, this operation is `GET /contacts` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

