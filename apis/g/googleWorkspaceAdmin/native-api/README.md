# Google Workspace Admin: Native API Reference

A consolidated summary of Google Workspace Admin's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/admin/directory/reference/rest
- **OpenAPI specification:** https://admin.googleapis.com/$discovery/rest?version=directory_v1
- **API base URL:** `https://admin.googleapis.com`

## Authentication

### Service Account

Authenticate Google Workspace Admin with a Google Cloud service account using Domain-Wide Delegation.

### Credentials

- **Service Account Client ID:** `clientId` · required · Required for Domain-Wide Delegation. Enter the numeric client_id from the service account JSON. A Google Workspace super admin must authorize this exact client ID in Admin console > API controls > Manage Domain Wide Delegation before this connection can work.
- **Client Email:** `clientEmail` · required · Enter the client_email value from the service account JSON key. This is the service account identity that MindCloud uses to request delegated access.
- **Private Key ID:** `privateKeyId` · required · Enter the private_key_id value from the service account JSON key. This helps identify which service account key is being used.
- **Private Key:** `privateKeySecret` · required · Enter the private_key value from the service account JSON key exactly as provided, including the BEGIN and END PRIVATE KEY lines. Keep this value secret.
- **Delegated Admin Email:** `delegatedAdminEmail` · required · Enter the email address of the Google Workspace admin user that MindCloud should impersonate. This must be a super admin or a delegated admin that already has the required user, group, and organizational unit privileges.

[Official authentication documentation](https://support.google.com/a/answer/162106?hl=en-EN)

## API conventions

The next-page cursor is read from `nextPageToken`.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Group Member](actions/add-group-member.md) | `POST /admin/directory/v1/groups/:groupKey/members` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/insert) |
| [Add Organizational Unit](actions/add-organizational-unit.md) | `POST /admin/directory/v1/customer/:customerId/orgunits` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/insert) |
| [Add User Alias](actions/add-user-alias.md) | `POST /admin/directory/v1/users/:userKey/aliases` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/insert) |
| [Check Group Membership](actions/check-group-membership.md) | `GET /admin/directory/v1/groups/:groupKey/hasMember/:memberKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/hasMember) |
| [Create Group](actions/create-group.md) | `POST /admin/directory/v1/groups` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/insert) |
| [Create User](actions/create-user.md) | `POST /admin/directory/v1/users` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/insert) |
| [Delete Group](actions/delete-group.md) | `DELETE /admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/delete) |
| [Delete User](actions/delete-user.md) | `DELETE /admin/directory/v1/users/:userKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/delete) |
| [Get Group](actions/get-group.md) | `GET /admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/get) |
| [Get Group Member](actions/get-group-member.md) | `GET /admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/get) |
| [Get Organizational Unit](actions/get-organizational-unit.md) | `GET /admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/get) |
| [Get User](actions/get-user.md) | `GET /admin/directory/v1/users/:userKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/get) |
| [Get User Photo](actions/get-user-photo.md) | `GET /admin/directory/v1/users/:userKey/photos/thumbnail` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.photos/get) |
| [List Group Members](actions/list-group-members.md) | `GET /admin/directory/v1/groups/:groupKey/members` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/list) |
| [List Groups](actions/list-groups.md) | `GET /admin/directory/v1/groups` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/list) |
| [List Organizational Units](actions/list-organizational-units.md) | `GET /admin/directory/v1/customer/:customerId/orgunits` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/list) |
| [List User Aliases](actions/list-user-aliases.md) | `GET /admin/directory/v1/users/:userKey/aliases` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/list) |
| [List Users](actions/list-users.md) | `GET /admin/directory/v1/users` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/list) |
| [Remove Group Member](actions/remove-group-member.md) | `DELETE /admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/delete) |
| [Remove Organizational Unit](actions/remove-organizational-unit.md) | `DELETE /admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/delete) |
| [Remove User Alias](actions/remove-user-alias.md) | `DELETE /admin/directory/v1/users/:userKey/aliases/:alias` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users.aliases/delete) |
| [Undelete User](actions/undelete-user.md) | `POST /admin/directory/v1/users/:userKey/undelete` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/undelete) |
| [Update Group](actions/update-group.md) | `PUT /admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/groups/update) |
| [Update Group Member](actions/update-group-member.md) | `PUT /admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/members/update) |
| [Update Organizational Unit](actions/update-organizational-unit.md) | `PUT /admin/directory/v1/customer/:customerId/orgunits/:orgUnitPath` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/orgunits/update) |
| [Update User](actions/update-user.md) | `PUT /admin/directory/v1/users/:userKey` | [docs](https://developers.google.com/workspace/admin/directory/reference/rest/v1/users/update) |
