# Superchat: Update Contact

Updates an existing contact in Superchat.

```
PUT https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_id` | string | yes | The unique identifier of the contact |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `first_name` | string | no | The first name of the contact |
| `last_name` | string | no | The last name of the contact |
| `gender` | string | no | The gender of the contact |
| `handles[]` | array<object> | no | The contact handles associated with this contact. Only supported for phone and email handles. |
| `custom_attributes[]` | array<object> | no | The contact attributes of this contact |

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

Through the native Superchat API, this operation is `PATCH /contacts/{contact_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

