# FileCloud: Native API Reference

A consolidated summary of FileCloud's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://fcapi-v1.filecloud.com/
- **OpenAPI specification:** https://fcapi-v1.filecloud.com/fc_api_v1_openapi-23.261.yaml
- **API base URL:** `https://mindcloud.filecloudtrial.com/api/v1`

## Authentication

### OAuth 2.0

Machine-to-machine OAuth 2.0 client credentials for FileCloud SCIM.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://mindcloud.filecloudtrial.com/api/v1/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `scim.read scim.write`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.filecloud.com/fcdoc/latest/server/filecloud-administrator-guide/filecloud-site-setup/client-security-settings/configuring-oauth-for-scim-integration)

## API conventions

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /scim/Groups` | [docs](https://fcapi-v1.filecloud.com/#/scim/createScimGroup) |
| [Delete Group](actions/delete-group.md) | `DELETE /scim/Groups/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/deleteScimGroup) |
| [Get Group by ID](actions/get-group-by-id.md) | `GET /scim/Groups/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/getScimGroupById) |
| [Get Resource Type by Name](actions/get-resource-type-by-name.md) | `GET /scim/ResourceTypes/:name` | [docs](https://fcapi-v1.filecloud.com/#/scim/getResourceTypeByName) |
| [Get Service Provider Configuration](actions/get-service-provider-configuration.md) | `GET /scim/ServiceProviderConfig` | [docs](https://fcapi-v1.filecloud.com/#/scim/getServiceProviderConfig) |
| [Get User by ID](actions/get-user-by-id.md) | `GET /scim/Users/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/getScimUserById) |
| [List Groups](actions/list-groups.md) | `GET /scim/Groups` | [docs](https://fcapi-v1.filecloud.com/#/scim/listScimGroups) |
| [List Resource Types](actions/list-resource-types.md) | `GET /scim/ResourceTypes` | [docs](https://fcapi-v1.filecloud.com/#/scim/getResourceTypes) |
| [List Schemas](actions/list-schemas.md) | `GET /scim/Schemas` | [docs](https://fcapi-v1.filecloud.com/#/scim/getSchemas) |
| [List Users](actions/list-users.md) | `GET /scim/Users` | [docs](https://fcapi-v1.filecloud.com/#/scim/listScimUsers) |
| [Patch User](actions/patch-user.md) | `PATCH /scim/Users/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/patchScimUser) |
| [Update Group](actions/update-group.md) | `PUT /scim/Groups/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/updateScimGroup) |
| [Update User](actions/update-user.md) | `PUT /scim/Users/:id` | [docs](https://fcapi-v1.filecloud.com/#/scim/updateScimUser) |
