# Flokzu: Native API Reference

A consolidated summary of Flokzu's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://flokzu.docs.apiary.io/reference/
- **API base URL:** `https://app.flokzu.com/flokzuopenapi/api`

## Authentication

### API Key

Flokzu API key auth using the user-specific API key plus username header.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Flokzu username used with the X-Username request header.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
X-Username: <username>
```

[Official authentication documentation](https://docs.flokzu.com/en/article/what-is-an-api-key-how-to-generate-it-1qrjbmn/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Record](actions/add-record.md) | `POST /v2/database/record` | [docs](https://flokzu.docs.apiary.io/reference/data-bases/add-record) |
| [Add User Role](actions/add-user-role.md) | `POST /v1/management/user/roles` | [docs](https://flokzu.docs.apiary.io/reference/users-management/roles/add-user-role) |
| [Create Process Instance](actions/create-process-instance.md) | `POST /v2/process/instance` | [docs](https://flokzu.docs.apiary.io/reference/process-instances/new-process-instance) |
| [Delete User Account](actions/delete-user-account.md) | `DELETE /v1/management/user` | [docs](https://flokzu.docs.apiary.io/reference/users-management/users/delete-user-account) |
| [Echo](actions/echo.md) | `POST /commons/JSON/echo` | [docs](https://flokzu.docs.apiary.io/reference/) |
| [Get Process Instance](actions/get-process-instance.md) | `GET /v2/process/instance` | [docs](https://flokzu.docs.apiary.io/reference/process-instances/get-process-instance) |
| [Get Record](actions/get-record.md) | `GET /v2/database/record` | [docs](https://flokzu.docs.apiary.io/reference/data-bases/get-record) |
| [List Assignees](actions/list-assignees.md) | `GET /commons/assignee/list` | [docs](https://flokzu.docs.apiary.io/reference/commons/assignees/get-assignee-list) |
| [List Records](actions/list-records.md) | `GET /v2/database/records` | [docs](https://flokzu.docs.apiary.io/reference/data-bases/list-records) |
| [List User Roles](actions/list-user-roles.md) | `GET /v1/management/user/roles` | [docs](https://flokzu.docs.apiary.io/reference/users-management/roles/get-user-roles) |
| [Operations](actions/operations.md) | `POST /commons/MATH/operations` | [docs](https://flokzu.docs.apiary.io/reference/commons/operations) |
| [Remove User Role](actions/remove-user-role.md) | `DELETE /v1/management/user/roles` | [docs](https://flokzu.docs.apiary.io/reference/users-management/roles/remove-user-role) |
| [Send New User Invitation](actions/send-new-user-invitation.md) | `POST /v1/management/user/invitation` | [docs](https://flokzu.docs.apiary.io/reference/users-management/users/send-new-user-invitation) |
| [Update Process Instance](actions/update-process-instance.md) | `PUT /v2/process/instance` | [docs](https://flokzu.docs.apiary.io/reference/process-instances/update-process-instance) |
| [Update Record](actions/update-record.md) | `PUT /v2/database/record` | [docs](https://flokzu.docs.apiary.io/reference/data-bases/update-record) |
