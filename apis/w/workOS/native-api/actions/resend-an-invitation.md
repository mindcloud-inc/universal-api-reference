# Resend an invitation with WorkOS

Resends an invitation in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/invitations/{id}/resend`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Resend an invitation](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the invitation. |
| `locale` | body | `string` | no | The locale to use when rendering the invitation email. See [supported locales](/authkit/hosted-ui/localization). |
