# Send an invitation with WorkOS

Sends an invitation in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/invitations`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Send an invitation](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the recipient. |
| `organization_id` | body | `string` | no | The ID of the [organization](/reference/organization) that the recipient will join. |
| `role_slug` | body | `string` | no | The [role](/authkit/roles) that the recipient will receive when they join the organization in the invitation. |
| `expires_in_days` | body | `number` | no | How many days the invitations will be valid for. Must be between 1 and 30 days. Defaults to 7 days if not specified. |
| `inviter_user_id` | body | `string` | no | The ID of the [user](/reference/authkit/user) who invites the recipient. The invitation email will mention the name of this user. |
| `locale` | body | `string` | no | The locale to use when rendering the invitation email. See [supported locales](/authkit/hosted-ui/localization). |
| `email` | body | `string` | yes | The email address of the recipient. |
| `organization_id` | body | `string` | no | The ID of the [organization](/reference/organization) that the recipient will join. |
| `role_slug` | body | `string` | no | The [role](/authkit/roles) that the recipient will receive when they join the organization in the invitation. |
| `expires_in_days` | body | `number` | no | How many days the invitations will be valid for. Must be between 1 and 30 days. Defaults to 7 days if not specified. |
| `inviter_user_id` | body | `string` | no | The ID of the [user](/reference/authkit/user) who invites the recipient. The invitation email will mention the name of this user. |
| `locale` | body | `string` | no | The locale to use when rendering the invitation email. See [supported locales](/authkit/hosted-ui/localization). |
