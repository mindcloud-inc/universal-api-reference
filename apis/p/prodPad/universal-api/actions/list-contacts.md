# ProdPad: List Contacts

Retrieves contacts from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-contacts?${params}`, {
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
| `company` | string | no |  |
| `persona` | string | no |  |
| `jobRole` | string | no |  |
| `tags` | string | no | Accepts multiple values in one string, delimited by `,`. |
| `name` | string | no |  |
| `externalId` | string | no |  |
| `externalUrl` | string | no |  |
| `email` | string | no |  |
| `feedbacks` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_count": 1,
      "contacts": [
        {
          "about": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen",
          "phone": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "include": {
        "deleted": true,
        "feedbacks": true,
        "numeric_id": true
      },
      "page": 1,
      "size": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_count` | number |  |
| `contacts[].about` | string |  |
| `contacts[].created_at` | date |  |
| `contacts[].email` | string |  |
| `contacts[].id` | string |  |
| `contacts[].name` | string |  |
| `contacts[].phone` | string |  |
| `contacts[].updated_at` | date |  |
| `include.deleted` | boolean |  |
| `include.feedbacks` | boolean |  |
| `include.numeric_id` | boolean |  |
| `page` | number |  |
| `size` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /contacts` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

