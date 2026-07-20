# Create an Organization with WorkOS

Creates an organization in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create an Organization](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the organization. |
| `allow_profiles_outside_organization` | body | `boolean` | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | body | `list<string>` | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | body | `list<object>` | no | The domains associated with the organization, including verification state. |
| `metadata` | body | `object` | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | body | `string` | no | An external identifier for the Organization. |
| `name` | body | `string` | yes | The name of the organization. |
| `allow_profiles_outside_organization` | body | `boolean` | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | body | `list<string>` | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | body | `list<object>` | no | The domains associated with the organization, including verification state. |
| `metadata` | body | `object` | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | body | `string` | no | An external identifier for the Organization. |
