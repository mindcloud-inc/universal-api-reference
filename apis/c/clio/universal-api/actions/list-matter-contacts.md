# Clio Manage: List Matter Contacts

Retrieves contacts for a matter in Clio Manage.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&matterId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "matterId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-contacts?${params}`, {
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
| `matterId` | number | yes | The Clio matter ID. |

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

Through the native Clio Manage API, this operation is `GET /matters/:matter_id/contacts.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-matter-contacts.md) for the provider-specific parameters and requirements.

