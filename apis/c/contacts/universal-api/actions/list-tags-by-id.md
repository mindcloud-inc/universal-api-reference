# Contacts+: List Tags by ID

Retrieves tags from Contacts+ by ID.

```
GET https://connect.mindcloud.co/v1/universal/contacts/latest/actions/list-tags-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/list-tags-by-id?connectionId=$CONNECTION_ID&tagIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/list-tags-by-id?${params}`, {
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
| `tagIds[]` | array<string> | yes | The tag IDs to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Retrieve tags from this team instead of personal tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "tagData": {
        "name": "Ava Chen"
      },
      "tagId": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `etag` | string |  |
| `tagData.name` | string |  |
| `tagId` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/tags.get` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags-by-id.md) for the provider-specific parameters and requirements.

