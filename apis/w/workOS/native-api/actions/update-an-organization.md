# Update an Organization with WorkOS

Updates an organization in your WorkOS environment.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/{id}`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Update an Organization](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the Organization. |
| `name` | body | `string` | no | The name of the organization. |
| `allow_profiles_outside_organization` | body | `boolean` | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | body | `list<string>` | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | body | `list<object>` | no | The domains associated with the organization, including verification state. |
| `stripe_customer_id` | body | `string` | no | The Stripe customer ID associated with the organization. |
| `metadata` | body | `object` | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | body | `string` | no | An external identifier for the Organization. |
| `id` | path | `string` | yes | Unique identifier of the Organization. |
| `name` | body | `string` | no | The name of the organization. |
| `allow_profiles_outside_organization` | body | `boolean` | no | Whether the organization allows profiles from outside the organization to sign in. |
| `domains` | body | `list<string>` | no | The domains associated with the organization. Deprecated in favor of `domain_data`. |
| `domain_data` | body | `list<object>` | no | The domains associated with the organization, including verification state. |
| `stripe_customer_id` | body | `string` | no | The Stripe customer ID associated with the organization. |
| `metadata` | body | `object` | no | Object containing [metadata](/authkit/metadata) key/value pairs associated with the Organization. |
| `external_id` | body | `string` | no | An external identifier for the Organization. |
