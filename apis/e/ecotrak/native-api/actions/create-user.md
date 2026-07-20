# Create User with Ecotrak

Creates a new user in Ecotrak.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/user`
- **Base URL:** `https://api.ecotrak.com`
- **Official documentation:** [Create User](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `number` | yes | Ecotrak company ID. |
| `email` | body | `string` | yes | User email address. |
| `first_name` | body | `string` | yes | User first name. |
| `last_name` | body | `string` | yes | User last name. |
| `job_title_id` | body | `number` | yes | Ecotrak job title ID. |
| `sso_user` | body | `boolean` | yes | Whether the user authenticates via SSO. |
| `password` | body | `string` | no | Password for non-SSO users. |
| `timezone` | body | `string` | yes | User timezone. |
| `nte_limit` | body | `number` | yes | Maximum not-to-exceed limit. |
