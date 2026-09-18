# Create User with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create User](https://api.gocanvas.com/api/v3/docs#create-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | — |
| `last_name` | body | `string` | yes | — |
| `email` | body | `string` | yes | — |
| `department_id` | body | `number` | no | Required when Departments are enabled for the GoCanvas company. |
| `department_role` | body | `list<string>` | yes | Accepted values: `department_admin`, `department_designer`, `department_dispatcher`, `department_reporter`, `department_user`. |
| `account_role` | body | `list<string>` | no | Only used when Departments are enabled. Leave unset when no account-wide role should be assigned. Accepted values: `account_admin`, `account_reporter`. |
| `password` | body | `string` | no | Must meet the company password policy. If omitted, GoCanvas generates a password and sends a setup email unless Skip Welcome Email is enabled. |
| `phone` | body | `string` | no | — |
| `skip_welcome_email` | body | `boolean` | no | — |
