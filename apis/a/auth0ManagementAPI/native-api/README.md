# Auth0 Management: Native API Reference

A consolidated summary of Auth0 Management's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://dev.auth0.com/docs/api/management/v2
- **API base URL:** `https://{tenantDomain}/api/v2`

## Authentication

### OAuth2

### Credentials

- **Tenant Domain:** `tenantDomain` · required · Your Auth0 tenant domain, for example your-tenant.us.auth0.com

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.tenantDomain}}/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.tenantDomain}}/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read:client_grants create:client_grants delete:client_grants update:client_grants read:users update:users delete:users create:users read:users_app_metadata update:users_app_metadata delete:users_app_metadata create:users_app_metadata read:user_custom_blocks create:user_custom_blocks delete:user_custom_blocks create:user_tickets read:clients update:clients delete:clients create:clients read:client_keys update:client_keys delete:client_keys create:client_keys read:client_credentials update:client_credentials delete:client_credentials create:client_credentials read:connections update:connections delete:connections create:connections read:resource_servers update:resource_servers delete:resource_servers create:resource_servers read:device_credentials update:device_credentials delete:device_credentials create:device_credentials read:rules update:rules delete:rules create:rules read:rules_configs update:rules_configs delete:rules_configs read:hooks update:hooks delete:hooks create:hooks read:actions update:actions delete:actions create:actions read:email_provider update:email_provider delete:email_provider create:email_provider blacklist:tokens read:stats read:insights read:tenant_settings update:tenant_settings read:logs read:logs_users read:shields create:shields update:shields delete:shields read:anomaly_blocks delete:anomaly_blocks update:triggers read:triggers read:grants delete:grants read:guardian_factors update:guardian_factors read:guardian_enrollments delete:guardian_enrollments create:guardian_enrollment_tickets read:user_idp_tokens create:passwords_checking_job delete:passwords_checking_job read:custom_domains delete:custom_domains create:custom_domains update:custom_domains read:email_templates create:email_templates update:email_templates read:mfa_policies update:mfa_policies read:roles create:roles delete:roles update:roles read:prompts update:prompts read:branding update:branding delete:branding read:log_streams create:log_streams delete:log_streams update:log_streams create:signing_keys read:signing_keys update:signing_keys read:limits update:limits create:role_members read:role_members delete:role_members read:entitlements read:attack_protection update:attack_protection read:organizations_summary create:authentication_methods read:authentication_methods update:authentication_methods delete:authentication_methods read:organizations update:organizations create:organizations delete:organizations read:organization_discovery_domains update:organization_discovery_domains create:organization_discovery_domains delete:organization_discovery_domains create:organization_members read:organization_members delete:organization_members create:organization_connections read:organization_connections update:organization_connections delete:organization_connections create:organization_member_roles read:organization_member_roles delete:organization_member_roles create:organization_invitations read:organization_invitations delete:organization_invitations read:scim_config create:scim_config update:scim_config delete:scim_config create:scim_token read:scim_token delete:scim_token read:directory_provisionings create:directory_provisionings update:directory_provisionings delete:directory_provisionings delete:phone_providers create:phone_providers read:phone_providers update:phone_providers delete:phone_templates create:phone_templates read:phone_templates update:phone_templates create:encryption_keys read:encryption_keys update:encryption_keys delete:encryption_keys read:sessions update:sessions delete:sessions read:refresh_tokens update:refresh_tokens delete:refresh_tokens create:self_service_profiles read:self_service_profiles update:self_service_profiles delete:self_service_profiles create:sso_access_tickets delete:sso_access_tickets read:forms update:forms delete:forms create:forms read:flows update:flows delete:flows create:flows read:flows_vault read:flows_vault_connections update:flows_vault_connections delete:flows_vault_connections create:flows_vault_connections read:flows_executions delete:flows_executions read:connections_options update:connections_options read:self_service_profile_custom_texts update:self_service_profile_custom_texts create:network_acls update:network_acls read:network_acls delete:network_acls delete:vdcs_templates read:vdcs_templates create:vdcs_templates update:vdcs_templates create:custom_signing_keys read:custom_signing_keys update:custom_signing_keys delete:custom_signing_keys read:federated_connections_tokens delete:federated_connections_tokens create:user_attribute_profiles read:user_attribute_profiles update:user_attribute_profiles delete:user_attribute_profiles read:event_streams create:event_streams delete:event_streams update:event_streams read:event_deliveries update:event_deliveries create:connection_profiles read:connection_profiles update:connection_profiles delete:connection_profiles create:group_roles delete:group_roles read:user_effective_permissions read:user_effective_roles read:organization_member_effective_roles read:user_role_source_groups read:organization_member_role_source_groups read:user_permission_source_roles read:group_roles read:organization_groups create:organization_groups delete:organization_groups read:organization_group_roles create:organization_group_roles delete:organization_group_roles create:token_exchange_profiles read:token_exchange_profiles update:token_exchange_profiles delete:token_exchange_profiles read:organization_client_grants create:organization_client_grants delete:organization_client_grants read:security_metrics read:connections_keys update:connections_keys create:connections_keys`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://auth0.com/docs/secure/tokens/access-tokens/management-api-access-tokens/get-management-api-access-tokens-for-production)

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Organization Members](actions/add-organization-members.md) | `POST /organizations/{id}/members` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Assign User Roles](actions/assign-user-roles.md) | `POST /users/{id}/roles` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Clients) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Create Role](actions/create-role.md) | `POST /roles` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Clients) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /organizations/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Delete Organization Connection](actions/delete-organization-connection.md) | `DELETE /organizations/{id}/enabled_connections/{connection_id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Delete Role](actions/delete-role.md) | `DELETE /roles/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [Enable Organization Connection](actions/enable-organization-connection.md) | `POST /organizations/{id}/enabled_connections` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Get Client](actions/get-client.md) | `GET /clients/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Clients) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Get Role](actions/get-role.md) | `GET /roles/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [Get User](actions/get-user.md) | `GET /users/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Clients) |
| [List Organization Connections](actions/list-organization-connections.md) | `GET /organizations/{id}/enabled_connections` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/{id}/members` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [List Role Permissions](actions/list-role-permissions.md) | `GET /roles/{id}/permissions` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [List Role Users](actions/list-role-users.md) | `GET /roles/{id}/users` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [List User Roles](actions/list-user-roles.md) | `GET /users/{id}/roles` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users/get_users) |
| [Remove Organization Members](actions/remove-organization-members.md) | `DELETE /organizations/{id}/members` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Remove User Roles](actions/remove-user-roles.md) | `DELETE /users/{id}/roles` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
| [Update Client](actions/update-client.md) | `PATCH /clients/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Clients) |
| [Update Organization](actions/update-organization.md) | `PATCH /organizations/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Organizations) |
| [Update Role](actions/update-role.md) | `PATCH /roles/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Roles) |
| [Update User](actions/update-user.md) | `PATCH /users/{id}` | [docs](https://dev.auth0.com/docs/api/management/v2#!/Users) |
