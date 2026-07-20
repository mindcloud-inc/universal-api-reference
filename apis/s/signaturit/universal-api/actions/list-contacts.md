# Signaturit: List Contacts

Retrieves contacts from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-contacts?${params}`, {
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
| `limit` | number | no | Maximum number of contacts to return. Default: `100`. Example: `100`. |
| `offset` | number | no | Results offset. Default: `0`. Example: `0`. |
| `email` | string | no | Filter contacts by email. Example: `sandbox-contact-20260318@example.com`. |
| `name` | string | no | Filter contacts by name. Example: `Sandbox Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /contacts.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

