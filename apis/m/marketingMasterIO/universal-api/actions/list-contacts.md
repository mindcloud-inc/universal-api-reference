# Marketing Master IO: List Contacts

Retrieves contacts from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-contacts?${params}`, {
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
| `book_id` | string | no | Filter contacts by contact book ID. |
| `tag` | string | no | Filter contacts by tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "book_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "phone_number": "string",
      "subscriber": true,
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `book_id` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `phone_number` | string |  |
| `subscriber` | boolean |  |
| `tag` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/contacts/list` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

