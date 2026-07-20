# Dashform: Get Form

Retrieves a form from Dashform.

```
GET https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-form?connectionId=$CONNECTION_ID&id=form_123%20or%20public_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "form_123 or public_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-form?${params}`, {
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
| `id` | string | yes | Dashform form ID or public ID from the list action. Example: `form_123 or public_123`. |

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
| `updated_at` | string | Last update timestamp |
| `user_id` | string | Creating user identifier |

## Native endpoint

Through the native Dashform API, this operation is `GET /api/v1/forms/:id` (base URL `https://getaiform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

