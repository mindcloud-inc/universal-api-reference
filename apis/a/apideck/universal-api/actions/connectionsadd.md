# Apideck: Create connection

Creates an authorized connection in Apideck Vault.

```
POST https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsadd
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsadd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service_id": "string",
  "unified_api": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsadd', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service_id": "string",
    "unified_api": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service_id` | string | yes |  |
| `unified_api` | string | yes |  |
| `id` | string | no |  |
| `service_id` | string | no |  |
| `name` | string | no |  |
| `tag_line` | string | no |  |
| `unified_api` | string | no |  |
| `state` | string | no |  |
| `integration_state` | string | no |  |
| `auth_type` | string | no |  |
| `oauth_grant_type` | string | no |  |
| `status` | string | no |  |
| `enabled` | boolean | no |  |
| `website` | string | no |  |
| `icon` | string | no |  |
| `logo` | string | no |  |
| `authorize_url` | string | no |  |
| `revoke_url` | string | no |  |
| `settings` | object | no |  |
| `metadata` | object | no |  |
| `form_fields` | list<object> | no |  |
| `configuration` | list<object> | no |  |
| `configurable_resources` | list<string> | no |  |
| `resource_schema_support` | list<string> | no |  |
| `resource_settings_support` | list<string> | no |  |
| `validation_support` | boolean | no |  |
| `schema_support` | boolean | no |  |
| `settings_required_for_authorization` | list<string> | no |  |
| `subscriptions` | list<object> | no |  |
| `has_guide` | boolean | no |  |
| `custom_mappings` | list<object> | no |  |
| `consent_state` | string | no |  |
| `consents` | list<object> | no |  |
| `latest_consent` | object | no |  |
| `application_data_scopes` | object | no |  |
| `health` | string | no |  |
| `credentials_expire_at` | number | no |  |
| `last_refresh_failed_at` | number | no |  |
| `created_at` | number | no |  |
| `updated_at` | number | no |  |

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

Through the native Apideck API, this operation is `POST /vault/connections/:unified_api/:service_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connectionsadd.md) for the provider-specific parameters and requirements.

