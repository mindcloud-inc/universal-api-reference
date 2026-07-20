# Flexmail: List Contacts

Retrieves contact records from your Flexmail account.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | An email address to filter on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_fields": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "language": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_fields` | object | Custom field values keyed by field name. |
| `email` | string | The email address of the contact. |
| `first_name` | string | The first name of the contact. |
| `id` | number | The identifier of the contact. |
| `language` | string | The contact language. |
| `name` | string | The last name of the contact. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /contacts` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

