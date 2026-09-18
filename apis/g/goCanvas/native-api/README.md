# GoCanvas: Native API Reference

A consolidated summary of GoCanvas's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://api.gocanvas.com/api/v3/docs
- **API base URL:** `https://www.gocanvas.com/api/v3`

## Authentication

### Basic Auth

Connect using your GoCanvas username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.gocanvas.com/api/v3/docs#authentication-basic)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User to Department](actions/add-user-to-department.md) | `POST /departments/:departmentId/users` | [docs](https://api.gocanvas.com/api/v3/docs#add-a-user-to-a-department) |
| [Assign User to Form](actions/assign-user-to-form.md) | `POST /forms/:formId/assigned_users` | [docs](https://api.gocanvas.com/api/v3/docs#assign-user-to-form) |
| [Change User Password](actions/change-user-password.md) | `PATCH /users/:userId/change_password` | [docs](https://api.gocanvas.com/api/v3/docs#change-user-password) |
| [Create Reference Data](actions/create-reference-data.md) | `POST /reference_data` | [docs](https://api.gocanvas.com/api/v3/docs#create-reference-data) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://api.gocanvas.com/api/v3/docs#create-a-user) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://api.gocanvas.com/api/v3/docs#current-user-profile) |
| [List Department Users](actions/list-department-users.md) | `GET /departments/:departmentId/users` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-department-users) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-departments) |
| [List Form Users](actions/list-form-users.md) | `GET /forms/:formId/assigned_users` | [docs](https://api.gocanvas.com/api/v3/docs#assigned-users-for-form) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-forms) |
| [List Reference Data](actions/list-reference-data.md) | `GET /reference_data` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-reference-data) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.gocanvas.com/api/v3/docs#list-all-users) |
| [Retrieve Reference Data](actions/retrieve-reference-data.md) | `GET /reference_data/:referenceDataId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-reference-data) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#retrieve-a-user) |
| [Unassign User from Form](actions/unassign-user-from-form.md) | `DELETE /forms/:formId/assigned_users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#unassign-user-from-form) |
| [Update Reference Data](actions/update-reference-data.md) | `PATCH /reference_data/:referenceDataId` | [docs](https://api.gocanvas.com/api/v3/docs#update-reference-data) |
| [Update User](actions/update-user.md) | `PATCH /users/:userId` | [docs](https://api.gocanvas.com/api/v3/docs#update-user) |
