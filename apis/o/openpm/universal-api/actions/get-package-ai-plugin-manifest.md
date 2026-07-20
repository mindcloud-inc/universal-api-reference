# openpm: Get Package AI Plugin Manifest



```
GET https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-ai-plugin-manifest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openpm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-ai-plugin-manifest?connectionId=$CONNECTION_ID&packageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-ai-plugin-manifest?${params}`, {
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
      "api": {},
      "auth": {},
      "contact_email": "ava@example.com",
      "description_for_human": "string",
      "description_for_model": "string",
      "legal_info_url": "https://example.com",
      "logo_url": "https://example.com",
      "name_for_human": "Ava Chen",
      "name_for_model": "Ava Chen",
      "schema_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api` | object | Plugin API configuration. |
| `auth` | object | Plugin authentication configuration. |
| `contact_email` | string | Plugin contact email. |
| `description_for_human` | string | Human-readable plugin description. |
| `description_for_model` | string | Model-facing plugin description. |
| `legal_info_url` | string | Plugin legal information URL. |
| `logo_url` | string | Plugin logo URL. |
| `name_for_human` | string | Human-readable plugin name. |
| `name_for_model` | string | Model-facing plugin name. |
| `schema_version` | string | AI plugin manifest schema version. |

## Native endpoint

Through the native openpm API, this operation is `GET /packages/:packageId/ai-plugin` (base URL `https://openpm.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-ai-plugin-manifest.md) for the provider-specific parameters and requirements.

