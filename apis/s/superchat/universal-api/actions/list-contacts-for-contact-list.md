# Superchat: List Contacts for Contact List

Retrieves contacts for a Superchat contact list.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-contacts-for-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-contacts-for-contact-list?connectionId=$CONNECTION_ID&limit=25&offset=0&contact_list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "contact_list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-contacts-for-contact-list?${params}`, {
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
| `contact_list_id` | string | yes | The unique identifier of the contact list |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Specify the cursor before which objects should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "custom_attributes": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string",
        "url": "https://example.com",
        "value": "string"
      },
      "first_name": "Ava",
      "gender": "string",
      "handles": {
        "id": "string",
        "type": "string",
        "value": "string"
      },
      "id": "string",
      "last_name": "Chen",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `custom_attributes` | array<object> |  |
| `custom_attributes.id` | string |  |
| `custom_attributes.name` | string |  |
| `custom_attributes.type` | string |  |
| `custom_attributes.url` | string |  |
| `custom_attributes.value` | string |  |
| `first_name` | string |  |
| `gender` | string |  |
| `handles` | array<object> |  |
| `handles.id` | string |  |
| `handles.type` | string |  |
| `handles.value` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `GET /contact-lists/{contact_list_id}/contacts` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-for-contact-list.md) for the provider-specific parameters and requirements.

