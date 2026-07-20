# Dashform: Update Form

Updates a form in Dashform.

```
PUT https://connect.mindcloud.co/v1/universal/dashform/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "form_123 or public_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashform/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "form_123 or public_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | New form description. |
| `id` | string | yes | Dashform form ID or public ID. Example: `form_123 or public_123`. |
| `name` | string | no | New form name. |
| `tone` | string | no | New tone or style. |
| `type` | string | no | New form type: structured or dynamic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "public_id": "string",
      "type": "string",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Form creation timestamp |
| `description` | string | Form description |
| `id` | string | Dashform form identifier |
| `name` | string | Form name |
| `organization_id` | string | Owning organization identifier |
| `public_id` | string | Public form identifier |
| `type` | string | Form type |
| `updated_at` | string | Last update timestamp |
| `user_id` | string | Creating user identifier |

## Native endpoint

Through the native Dashform API, this operation is `PATCH /api/v1/forms/:id` (base URL `https://getaiform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

