# Apideck: Get resource settings

Retrieves connection resource settings from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsettingsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsettingsall?connectionId=$CONNECTION_ID&unified_api=string&service_id=string&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unified_api": "string",
  "service_id": "string",
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsettingsall?${params}`, {
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
| `unified_api` | string | yes |  |
| `service_id` | string | yes |  |
| `resource` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application_data_scopes": {},
      "auth_type": "string",
      "authorize_url": "https://example.com",
      "configurable_resources": [
        "string"
      ],
      "configuration": [
        {}
      ],
      "consent_state": "string",
      "consents": [
        {}
      ],
      "created_at": 1,
      "credentials_expire_at": 1,
      "custom_mappings": [
        {}
      ],
      "enabled": true,
      "form_fields": [
        {}
      ],
      "has_guide": true,
      "health": "string",
      "icon": "string",
      "id": "string",
      "integration_state": "string",
      "last_refresh_failed_at": 1,
      "latest_consent": {},
      "logo": "string",
      "metadata": {},
      "name": "Ava Chen",
      "oauth_grant_type": "string",
      "resource_schema_support": [
        "string"
      ],
      "resource_settings_support": [
        "string"
      ],
      "revoke_url": "https://example.com",
      "schema_support": true,
      "service_id": "string",
      "settings": {},
      "settings_required_for_authorization": [
        "string"
      ],
      "state": "string",
      "status": "string",
      "subscriptions": [
        {}
      ],
      "tag_line": "string",
      "unified_api": "string",
      "updated_at": 1,
      "validation_support": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_data_scopes` | object |  |
| `auth_type` | string |  |
| `authorize_url` | string |  |
| `configurable_resources` | array<string> |  |
| `configuration` | array<object> |  |
| `consent_state` | string |  |
| `consents` | array<object> |  |
| `created_at` | number |  |
| `credentials_expire_at` | number |  |
| `custom_mappings` | array<object> |  |
| `enabled` | boolean |  |
| `form_fields` | array<object> |  |
| `has_guide` | boolean |  |
| `health` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `integration_state` | string |  |
| `last_refresh_failed_at` | number |  |
| `latest_consent` | object |  |
| `logo` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `oauth_grant_type` | string |  |
| `resource_schema_support` | array<string> |  |
| `resource_settings_support` | array<string> |  |
| `revoke_url` | string |  |
| `schema_support` | boolean |  |
| `service_id` | string |  |
| `settings` | object |  |
| `settings_required_for_authorization` | array<string> |  |
| `state` | string |  |
| `status` | string |  |
| `subscriptions` | array<object> |  |
| `tag_line` | string |  |
| `unified_api` | string |  |
| `updated_at` | number |  |
| `validation_support` | boolean |  |
| `website` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/connections/:unified_api/:service_id/:resource/config` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connectionsettingsall.md) for the provider-specific parameters and requirements.

