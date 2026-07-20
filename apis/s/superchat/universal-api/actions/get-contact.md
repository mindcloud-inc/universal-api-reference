# Superchat: Get Contact

Retrieves a contact from Superchat by ID.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-contact?${params}`, {
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
| `contact_id` | string | yes | The unique identifier of the contact |

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

Through the native Superchat API, this operation is `GET /contacts/{contact_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

