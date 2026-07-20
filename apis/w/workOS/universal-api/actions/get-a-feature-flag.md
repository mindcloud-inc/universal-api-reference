# WorkOS: Get a feature flag

Retrieves a feature flag from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-feature-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-feature-flag?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-feature-flag?${params}`, {
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
| `slug` | string | yes | A unique key to reference the Feature Flag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "default_value": true,
      "description": "string",
      "enabled": true,
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "object": "string",
      "owner": {},
      "slug": "string",
      "tags": [
        "string"
      ],
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
| `default_value` | boolean | The value returned for users and organizations who don't match any configured targeting rules. |
| `description` | string | A description for the Feature Flag. |
| `enabled` | boolean | Specifies whether the Feature Flag is active for the current environment. |
| `id` | string | Unique identifier of the Feature Flag. |
| `message` | string | WorkOS response field message. |
| `name` | string | A descriptive name for the Feature Flag. This field does not need to be unique. |
| `object` | string | Distinguishes the Feature Flag object. |
| `owner` | object | The owner of the Feature Flag. |
| `slug` | string | A unique key to reference the Feature Flag. |
| `tags` | array<string> | Labels assigned to the Feature Flag for categorizing and filtering. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /feature-flags/{slug}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-feature-flag.md) for the provider-specific parameters and requirements.

