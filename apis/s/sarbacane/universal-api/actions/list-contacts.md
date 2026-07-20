# Sarbacane: List Contacts

Retrieves contacts from a Sarbacane list.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Filter contacts by exact email address. |
| `end` | string | no | Filter contacts modified on or before this ISO timestamp. |
| `listId` | string | no | Sarbacane list ID. |
| `phone` | string | no | Filter contacts by exact phone number. |
| `search` | string | no | Search text across contact fields. |
| `start` | string | no | Filter contacts modified on or after this ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "edited": "string",
      "email": "ava@example.com",
      "id": "string",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Contact creation timestamp. |
| `edited` | string | Last modification timestamp. |
| `email` | string | Primary email address. |
| `id` | string | Sarbacane contact ID. |
| `phone` | string | Primary phone number. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /lists/{listId}/contacts` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

