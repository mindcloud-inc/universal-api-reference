# BASIC: Native API Reference

A consolidated summary of BASIC's API configuration and 64 documented operations, with links to official documentation.

- **Official docs:** https://docs.basic.tech/basic-restapi/basic-api
- **OpenAPI specification:** https://docs.basic.tech/openapi.json
- **API base URL:** `https://api.basic.tech`

## Authentication

### API Key

Use a BASIC project API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.basic.tech/basic-expo-rn/rn-adminportal)

## Endpoints (64 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept a team invite](actions/accept-a-team-invite.md) | `POST /team/accept-invite` | [docs](https://docs.basic.tech/api-reference/teams/accept-a-team-invite) |
| [Check auth endpoint status](actions/check-auth-endpoint-status.md) | `GET /auth/` | [docs](https://docs.basic.tech/api-reference/auth/check-auth-endpoint-status) |
| [Check project slug availability](actions/check-project-slug-availability.md) | `GET /project/slug` | [docs](https://docs.basic.tech/api-reference/projects/check-project-slug-availability) |
| [Check Root Endpoint Status](actions/check-root-endpoint-status.md) | `GET /` | [docs](https://docs.basic.tech/openapi.json) |
| [Check team slug availability](actions/check-team-slug-availability.md) | `GET /team/slug` | [docs](https://docs.basic.tech/api-reference/teams/check-team-slug-availability) |
| [Check Utils Endpoint Status](actions/check-utils-endpoint-status.md) | `GET /utils/` | [docs](https://docs.basic.tech/api-reference/utils/check-utils-endpoint-status) |
| [Compare two schemas](actions/compare-two-schemas.md) | `POST /utils/schema/compareSchema` | [docs](https://docs.basic.tech/api-reference/utils/compare-two-schemas) |
| [Convert text to URL-friendly slug](actions/convert-text-to-url-friendly-slug.md) | `GET /utils/slugify` | [docs](https://docs.basic.tech/api-reference/utils/convert-text-to-url-friendly-slug) |
| [Create a new project](actions/create-a-new-project.md) | `POST /project/` | [docs](https://docs.basic.tech/api-reference/projects/create-a-new-project) |
| [Create a new team](actions/create-a-new-team.md) | `POST /team/` | [docs](https://docs.basic.tech/api-reference/teams/create-a-new-team) |
| [Create a team invite](actions/create-a-team-invite.md) | `POST /team/{team_id}/invite` | [docs](https://docs.basic.tech/api-reference/teams/create-a-team-invite) |
| [Create item](actions/create-item.md) | `POST /project/{id}/user/{user_id}/db/{table_id}` | [docs](https://docs.basic.tech/api-reference/project-users/create-item) |
| [Create new API key](actions/create-new-api-key.md) | `POST /project/{id}/key` | [docs](https://docs.basic.tech/api-reference/project-keys/create-new-api-key) |
| [Delete a project](actions/delete-a-project.md) | `DELETE /project/{id}` | [docs](https://docs.basic.tech/api-reference/projects/delete-a-project) |
| [Delete a team](actions/delete-a-team.md) | `DELETE /team/{team_id}` | [docs](https://docs.basic.tech/openapi.json) |
| [Delete a team invite](actions/delete-a-team-invite.md) | `DELETE /team/{team_id}/invite/{invite_id}` | [docs](https://docs.basic.tech/api-reference/teams/delete-a-team-invite) |
| [Delete a team member](actions/delete-a-team-member.md) | `DELETE /team/{team_id}/member/{member_id}` | [docs](https://docs.basic.tech/api-reference/teams/delete-a-team-member) |
| [Delete a user from the project](actions/delete-a-user-from-the-project.md) | `DELETE /project/{id}/user/{user_id}` | [docs](https://docs.basic.tech/api-reference/project-users/delete-a-user-from-the-project) |
| [Delete an item](actions/delete-an-item.md) | `DELETE /project/{id}/user/{user_id}/db/{table_id}/{item_id}` | [docs](https://docs.basic.tech/api-reference/project-users/delete-an-item) |
| [Delete API key](actions/delete-api-key.md) | `DELETE /project/{id}/key/{key_id}` | [docs](https://docs.basic.tech/api-reference/project-keys/delete-api-key) |
| [Delete project background image](actions/delete-project-background-image.md) | `DELETE /project/{id}/upload/background` | [docs](https://docs.basic.tech/openapi.json) |
| [Delete project icon](actions/delete-project-icon.md) | `DELETE /project/{id}/upload/icon` | [docs](https://docs.basic.tech/openapi.json) |
| [Delete specific settings values](actions/delete-specific-settings-values.md) | `DELETE /project/{id}/settings` | [docs](https://docs.basic.tech/openapi.json) |
| [Generate or update suggested schema using AI](actions/generate-or-update-suggested-schema-using-ai.md) | `POST /project/{id}/schema/generate` | [docs](https://docs.basic.tech/openapi.json) |
| [Get all items in a table](actions/get-all-items-in-a-table.md) | `GET /project/{id}/user/{user_id}/db/{table_id}` | [docs](https://docs.basic.tech/api-reference/project-users/get-all-items) |
| [Get all keys for a project](actions/get-all-keys-for-a-project.md) | `GET /project/{id}/key` | [docs](https://docs.basic.tech/api-reference/project-keys/get-all-keys) |
| [Get all users in project](actions/get-all-users-in-project.md) | `GET /project/{id}/user/` | [docs](https://docs.basic.tech/api-reference/project-users/get-project-users) |
| [Get auth token](actions/get-auth-token.md) | `POST /auth/token` | [docs](https://docs.basic.tech/api-reference/auth/get-auth-token) |
| [Get client metadata document](actions/get-client-metadata-document.md) | `GET /projects/{id}/client-metadata.json` | [docs](https://docs.basic.tech/openapi.json) |
| [Get project activity stats](actions/get-project-activity-stats.md) | `GET /project/{id}/user/stats` | [docs](https://docs.basic.tech/openapi.json) |
| [Get project details](actions/get-project-details.md) | `GET /project/{id}` | [docs](https://docs.basic.tech/api-reference/projects/get-project-details) |
| [Get project DID document](actions/get-project-did-document.md) | `GET /projects/{hexId}/did.json` | [docs](https://docs.basic.tech/openapi.json) |
| [Get project images](actions/get-project-images.md) | `GET /project/{id}/upload` | [docs](https://docs.basic.tech/openapi.json) |
| [Get project public profile](actions/get-project-public-profile.md) | `GET /project/{id}/profile` | [docs](https://docs.basic.tech/openapi.json) |
| [Get project schema](actions/get-project-schema.md) | `GET /project/{id}/schema` | [docs](https://docs.basic.tech/api-reference/projects/get-project-schema) |
| [Get project settings](actions/get-project-settings.md) | `GET /project/{id}/settings` | [docs](https://docs.basic.tech/openapi.json) |
| [Get specific API key](actions/get-specific-api-key.md) | `GET /project/{id}/key/{key_id}` | [docs](https://docs.basic.tech/api-reference/project-keys/get-specific-api-key) |
| [Get specific item in a table](actions/get-specific-item-in-a-table.md) | `GET /project/{id}/user/{user_id}/db/{table_id}/{item_id}` | [docs](https://docs.basic.tech/api-reference/project-users/get-specific-item) |
| [Get team by ID](actions/get-team-by-id.md) | `GET /team/{team_id}` | [docs](https://docs.basic.tech/api-reference/teams/get-team-by-id) |
| [Get team invites](actions/get-team-invites.md) | `GET /team/{team_id}/invite` | [docs](https://docs.basic.tech/api-reference/teams/get-team-invites) |
| [Get team members](actions/get-team-members.md) | `GET /team/{team_id}/member` | [docs](https://docs.basic.tech/api-reference/teams/get-team-members) |
| [Get user details](actions/get-user-details.md) | `GET /project/{id}/user/{user_id}` | [docs](https://docs.basic.tech/api-reference/project-users/get-user-details) |
| [Get user info](actions/get-user-info.md) | `GET /auth/userinfo` | [docs](https://docs.basic.tech/api-reference/auth/get-user-info) |
| [Get user teams](actions/get-user-teams.md) | `GET /team/` | [docs](https://docs.basic.tech/api-reference/teams/get-user-teams) |
| [JSON Web Key Set](actions/j-son-web-key-set.md) | `GET /auth/.well-known/jwks.json` | [docs](https://docs.basic.tech/openapi.json) |
| [Get all admin projects of developer](actions/list-admin-projects.md) | `GET /project/` | [docs](https://docs.basic.tech/api-reference/projects/get-all-admin-projects) |
| [Merge and update project schema](actions/merge-and-update-project-schema.md) | `PATCH /project/{id}/schema` | [docs](https://docs.basic.tech/api-reference/projects/patch-project-schema) |
| [OpenID Connect Discovery Document](actions/open-id-connect-discovery-document.md) | `GET /auth/.well-known/openid-configuration` | [docs](https://docs.basic.tech/openapi.json) |
| [Redirect to sign in](actions/redirect-to-sign-in.md) | `GET /auth/authorize` | [docs](https://docs.basic.tech/api-reference/auth/redirect-to-sign-in) |
| [Regenerate API key](actions/regenerate-api-key.md) | `POST /project/{id}/key/{key_id}/regenerate` | [docs](https://docs.basic.tech/api-reference/project-keys/regenerate-api-key) |
| [Replace an item](actions/replace-an-item.md) | `PUT /project/{id}/user/{user_id}/db/{table_id}/{item_id}` | [docs](https://docs.basic.tech/api-reference/project-users/replace-an-item) |
| [Report a user connection to this project](actions/report-a-user-connection-to-this-project.md) | `POST /project/{id}/user/connect` | [docs](https://docs.basic.tech/openapi.json) |
| [Update a team](actions/update-a-team.md) | `PATCH /team/{team_id}` | [docs](https://docs.basic.tech/api-reference/teams/update-a-team) |
| [Update a team member](actions/update-a-team-member.md) | `PATCH /team/{team_id}/member/{member_id}` | [docs](https://docs.basic.tech/api-reference/teams/update-a-team-member) |
| [Update an item](actions/update-an-item.md) | `PATCH /project/{id}/user/{user_id}/db/{table_id}/{item_id}` | [docs](https://docs.basic.tech/api-reference/project-users/update-an-item-in-the-users-database-1) |
| [Update API key](actions/update-api-key.md) | `PATCH /project/{id}/key/{key_id}` | [docs](https://docs.basic.tech/api-reference/project-keys/update-api-key) |
| [Update project details](actions/update-project-details.md) | `PATCH /project/{id}` | [docs](https://docs.basic.tech/api-reference/projects/update-project-details) |
| [Update project schema](actions/update-project-schema.md) | `POST /project/{id}/schema` | [docs](https://docs.basic.tech/api-reference/projects/update-project-schema) |
| [Update project settings](actions/update-project-settings.md) | `PATCH /project/{id}/settings` | [docs](https://docs.basic.tech/openapi.json) |
| [Update user metadata](actions/update-user-metadata.md) | `PATCH /project/{id}/user/{user_id}` | [docs](https://docs.basic.tech/api-reference/project-users/update-user-details) |
| [Upload project background image](actions/upload-project-background-image.md) | `POST /project/{id}/upload/background` | [docs](https://docs.basic.tech/openapi.json) |
| [Upload project icon](actions/upload-project-icon.md) | `POST /project/{id}/upload/icon` | [docs](https://docs.basic.tech/openapi.json) |
| [Verify API key](actions/verify-api-key.md) | `POST /project/{id}/key/verify` | [docs](https://docs.basic.tech/api-reference/project-keys/verify-api-key) |
| [Verify update schema](actions/verify-update-schema.md) | `POST /utils/schema/verifyUpdateSchema` | [docs](https://docs.basic.tech/api-reference/utils/verify-update-schema) |
