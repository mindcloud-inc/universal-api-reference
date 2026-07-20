# Dashform: Create Form

Creates a form in Dashform.

```
POST https://connect.mindcloud.co/v1/universal/dashform/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Contact Form"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashform/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Contact Form"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional form description. Example: `A simple contact form`. |
| `name` | string | yes | Form name. Example: `Contact Form`. |
| `tone` | string | no | Optional tone or style for the form. Example: `formal`. |
| `type` | string | no | Form type: structured or dynamic. Example: `structured`. |

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

Through the native Dashform API, this operation is `POST /api/v1/forms` (base URL `https://getaiform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

