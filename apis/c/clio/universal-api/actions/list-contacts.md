# Clio Manage: List Contacts

Retrieves contacts from your Clio Manage account.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts?${params}`, {
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
| `query` | string | no | Wildcard search for contact name, title, email, address, phone number, website, instant messenger address, custom fields, related matter name, or company name. |
| `clientOnly` | boolean | no | Filter contacts to only those that are clients. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updatedSince` | date | no | Filter contacts to those updated after a specific ISO-8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1,
      "initials": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /contacts.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

