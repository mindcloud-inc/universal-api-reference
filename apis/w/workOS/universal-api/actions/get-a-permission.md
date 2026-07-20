# WorkOS: Get a permission

Retrieves a permission from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-permission?connectionId=$CONNECTION_ID&slug=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-permission?${params}`, {
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
| `slug` | string | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `slug` | string | yes | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "object": "string",
      "resource_type_slug": "string",
      "slug": "string",
      "system": true,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `description` | string | An optional description of the Permission. |
| `id` | string | Unique identifier of the Permission. |
| `message` | string | WorkOS response field message. |
| `name` | string | A descriptive name for the Permission. |
| `object` | string | Distinguishes the Permission object. |
| `resource_type_slug` | string | The slug of the resource type associated with the permission. |
| `slug` | string | A unique key to reference the permission. Must be lowercase and contain only letters, numbers, hyphens, underscores, colons, periods, and asterisks. |
| `system` | boolean | Whether the permission is a system permission. System permissions are managed by WorkOS and cannot be deleted. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /authorization/permissions/{slug}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-permission.md) for the provider-specific parameters and requirements.

