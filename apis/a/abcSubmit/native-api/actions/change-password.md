# Change Password with AbcSubmit

Updates a user's password in AbcSubmit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/users/change-password`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Change Password](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `old_password` | body | `string` | yes | The current password for the authenticated AbcSubmit account. |
| `new_password` | body | `string` | yes | The new password to apply to the authenticated account. |
| `confirm_password` | body | `string` | yes | Repeat the new password for confirmation. |
