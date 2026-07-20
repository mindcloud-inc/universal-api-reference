# openpm: Get Package



```
GET https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openpm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package?connectionId=$CONNECTION_ID&packageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package?${params}`, {
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
| `packageId` | string | yes | Package ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_email": "ava@example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "id": "string",
      "legal_info_url": "https://example.com",
      "logo_url": "https://example.com",
      "machine_description": "string",
      "machine_name": "Ava Chen",
      "name": "Ava Chen",
      "openapi": "string",
      "published_at": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_email` | string | Package contact email. |
| `created_at` | date | Package creation date. |
| `deleted_at` | date | Runtime deletion timestamp when present. |
| `description` | string | Package description. |
| `domain` | string | Package domain. |
| `id` | string | Package id. |
| `legal_info_url` | string | Package legal information URL. |
| `logo_url` | string | Package logo URL. |
| `machine_description` | string | Package description for machines. |
| `machine_name` | string | Package name for machines. |
| `name` | string | Package name. |
| `openapi` | string | Package OpenAPI specification. |
| `published_at` | date | Package publication date. |
| `updated_at` | date | Package last update date. |
| `user_id` | string | Package owner user id. |
| `version` | string | Package version. |

## Native endpoint

Through the native openpm API, this operation is `GET /packages/:packageId` (base URL `https://openpm.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package.md) for the provider-specific parameters and requirements.

