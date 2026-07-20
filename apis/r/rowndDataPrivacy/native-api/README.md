# Rownd Data Privacy: Native API Reference

A consolidated summary of Rownd Data Privacy's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.rownd.io/api-reference/authentication/overview
- **API base URL:** `https://api.rownd.io/applications/{appId}`

## Authentication

### Rownd App Credentials

Use the Rownd tenant app ID, app key, and app secret for app-scoped REST API access.

### Credentials

- **App ID:** `appId` · optional · Rownd application ID used in the base URL path for app-scoped endpoints.
- **App Key:** `appKey` · optional · Rownd publishable app key sent in the x-rownd-app-key header.
- **App Secret:** `appSecret` · optional · Rownd private app secret sent in the x-rownd-app-secret header.

Send these headers with each API request:

```http
x-rownd-app-key: <appKey>
x-rownd-app-secret: <appSecret>
```

[Official authentication documentation](https://docs.rownd.io/configuration/app-credentials)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://docs.rownd.io/api-reference/groups/platform/group-create) |
| [Create Group Invite](actions/create-group-invite.md) | `POST /groups/:group/invites` | [docs](https://docs.rownd.io/api-reference/groups/platform/invites/invite-create) |
| [Create Group Member](actions/create-group-member.md) | `POST /groups/:group/members` | [docs](https://docs.rownd.io/api-reference/groups/platform/members/member-create) |
| [Create Magic Link](actions/create-magic-link.md) | `POST https://api.rownd.io/hub/auth/magic` | [docs](https://docs.rownd.io/api-reference/authentication/create-magic-link) |
| [Create OIDC Client](actions/create-oidc-client.md) | `POST /oidc-clients` | [docs](https://docs.rownd.io/api-reference/oidc/clients/create) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:group` | [docs](https://docs.rownd.io/api-reference/groups/platform/group-delete) |
| [Delete Group Invite](actions/delete-group-invite.md) | `DELETE /groups/:group/invites/:invite` | [docs](https://docs.rownd.io/api-reference/groups/platform/invites/invite-delete) |
| [Delete Group Member](actions/delete-group-member.md) | `DELETE /groups/:group/members/:member` | [docs](https://docs.rownd.io/api-reference/groups/platform/members/member-delete) |
| [Delete OIDC Client](actions/delete-oidc-client.md) | `DELETE /oidc-clients/:client` | [docs](https://docs.rownd.io/api-reference/oidc/clients/delete) |
| [Delete User Profile](actions/delete-user-profile.md) | `DELETE /users/:user/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/delete) |
| [Get Sample User Profile Data](actions/get-sample-user-profile-data.md) | `GET /users/__sample__/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/get-sample-data) |
| [Insert or Update User Profile Data](actions/insert-or-update-user-profile-data.md) | `PUT /users/:user/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/insert-update) |
| [List Group Invites](actions/list-group-invites.md) | `GET /groups/:group/invites` | [docs](https://docs.rownd.io/api-reference/groups/platform/invites/invite-list) |
| [List Group Members](actions/list-group-members.md) | `GET /groups/:group/members` | [docs](https://docs.rownd.io/api-reference/groups/platform/members/member-list) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.rownd.io/api-reference/groups/platform/group-list) |
| [List OIDC Clients](actions/list-oidc-clients.md) | `GET /oidc-clients` | [docs](https://docs.rownd.io/api-reference/oidc/clients/list) |
| [List User Profiles](actions/list-user-profiles.md) | `GET /users/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/list-user-profiles) |
| [Retrieve Group](actions/retrieve-group.md) | `GET /groups/:group` | [docs](https://docs.rownd.io/api-reference/groups/platform/group-read) |
| [Retrieve Group Invite](actions/retrieve-group-invite.md) | `GET /groups/:group/invites/:invite` | [docs](https://docs.rownd.io/api-reference/groups/platform/invites/invite-read) |
| [Retrieve Group Member](actions/retrieve-group-member.md) | `GET /groups/:group/members/:member` | [docs](https://docs.rownd.io/api-reference/groups/platform/members/member-read) |
| [Retrieve JWK Set](actions/retrieve-jwk-set.md) | `GET https://api.rownd.io/hub/auth/keys` | [docs](https://docs.rownd.io/api-reference/authentication/retrieve-jwk) |
| [Retrieve OIDC Client](actions/retrieve-oidc-client.md) | `GET /oidc-clients/:client` | [docs](https://docs.rownd.io/api-reference/oidc/clients/read) |
| [Retrieve OIDC Configuration](actions/retrieve-oidc-configuration.md) | `GET https://api.rownd.io/hub/auth/.well-known/oauth-authorization-server` | [docs](https://docs.rownd.io/api-reference/authentication/retrieve-oidc) |
| [Retrieve User Profile](actions/retrieve-user-profile.md) | `GET /users/:user/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/get-user-data) |
| [Retrieve User Profile Field](actions/retrieve-user-profile-field.md) | `GET /users/:user/data/fields/:field` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/retrieve-field) |
| [Revoke User Sessions](actions/revoke-user-sessions.md) | `POST /users/:user/signout` | [docs](https://docs.rownd.io/api-reference/user-sessions/app/revoke-user-sessions) |
| [Update Group](actions/update-group.md) | `PUT /groups/:group` | [docs](https://docs.rownd.io/api-reference/groups/platform/group-update) |
| [Update Group Invite](actions/update-group-invite.md) | `PUT /groups/:group/invites/:invite` | [docs](https://docs.rownd.io/api-reference/groups/platform/invites/invite-update) |
| [Update Group Member](actions/update-group-member.md) | `PUT /groups/:group/members/:member` | [docs](https://docs.rownd.io/api-reference/groups/platform/members/member-update) |
| [Update OIDC Client](actions/update-oidc-client.md) | `PUT /oidc-clients/:client` | [docs](https://docs.rownd.io/api-reference/oidc/clients/update) |
| [Update User Profile Data](actions/update-user-profile-data.md) | `PATCH /users/:user/data` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/update-patch) |
| [Update User Profile Field](actions/update-user-profile-field.md) | `PUT /users/:user/data/fields/:field` | [docs](https://docs.rownd.io/api-reference/user-profiles/app/update-field) |
