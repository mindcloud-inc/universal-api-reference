# Update User with Ecotrak

Updates an existing user in Ecotrak.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/user/:user_id`
- **Base URL:** `https://api.ecotrak.com`
- **Official documentation:** [Update User](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-edit-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Ecotrak user ID. |
| `company_id` | body | `number` | yes | Ecotrak company ID. |
| `email` | body | `string` | yes | User email address. |
| `first_name` | body | `string` | yes | User first name. |
| `last_name` | body | `string` | yes | User last name. |
| `job_title_id` | body | `number` | yes | Ecotrak job title ID. |
| `sso_user` | body | `boolean` | yes | Whether the user authenticates via SSO. |
| `password` | body | `string` | no | Password for non-SSO users. |
| `timezone` | body | `string` | yes | User timezone. |
| `nte_limit` | body | `number` | yes | Maximum not-to-exceed limit. |
