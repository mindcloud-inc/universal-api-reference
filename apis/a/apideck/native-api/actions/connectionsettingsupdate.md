# Update settings with Apideck

Updates connection resource settings in Apideck Vault.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/vault/connections/:unified_api/:service_id/:resource/config`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Update settings](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `unified_api` | path | `string` | yes |
| `resource` | path | `string` | yes |
| `id` | body | `string` | no |
| `service_id` | body | `string` | no |
| `name` | body | `string` | no |
| `tag_line` | body | `string` | no |
| `unified_api` | body | `string` | no |
| `state` | body | `string` | no |
| `integration_state` | body | `string` | no |
| `auth_type` | body | `string` | no |
| `oauth_grant_type` | body | `string` | no |
| `status` | body | `string` | no |
| `enabled` | body | `boolean` | no |
| `website` | body | `string` | no |
| `icon` | body | `string` | no |
| `logo` | body | `string` | no |
| `authorize_url` | body | `string` | no |
| `revoke_url` | body | `string` | no |
| `settings` | body | `object` | no |
| `metadata` | body | `object` | no |
| `form_fields` | body | `list<object>` | no |
| `configuration` | body | `list<object>` | no |
| `configurable_resources` | body | `list<string>` | no |
| `resource_schema_support` | body | `list<string>` | no |
| `resource_settings_support` | body | `list<string>` | no |
| `validation_support` | body | `boolean` | no |
| `schema_support` | body | `boolean` | no |
| `settings_required_for_authorization` | body | `list<string>` | no |
| `subscriptions` | body | `list<object>` | no |
| `has_guide` | body | `boolean` | no |
| `custom_mappings` | body | `list<object>` | no |
| `consent_state` | body | `string` | no |
| `consents` | body | `list<object>` | no |
| `latest_consent` | body | `object` | no |
| `application_data_scopes` | body | `object` | no |
| `health` | body | `string` | no |
| `credentials_expire_at` | body | `number` | no |
| `last_refresh_failed_at` | body | `number` | no |
| `created_at` | body | `number` | no |
| `updated_at` | body | `number` | no |
