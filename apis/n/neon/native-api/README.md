# Neon: Native API Reference

A consolidated summary of Neon's API configuration and 140 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.neon.tech/reference
- **OpenAPI specification:** https://neon.com/api_spec/release/v2.json
- **API base URL:** `https://console.neon.tech/api/v2`

## Authentication

### Neon API Key

Use a Neon API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://neon.tech/docs/manage/api-keys/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (140 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept a project transfer request](actions/accept-project-transfer-request.md) | `PUT /projects/:project_id/transfer_requests/:request_id` | [docs](https://api-docs.neon.tech/reference/acceptprojecttransferrequest) |
| [Add a OAuth provider](actions/add-branch-neon-auth-oauth-provider.md) | `POST /projects/:project_id/branches/:branch_id/auth/oauth_providers` | [docs](https://api-docs.neon.tech/reference/addbranchneonauthoauthprovider) |
| [Add domain to redirect_uri whitelist](actions/add-branch-neon-auth-trusted-domain.md) | `POST /projects/:project_id/branches/:branch_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/addbranchneonauthtrusteddomain) |
| [Add domain to redirect_uri whitelist](actions/add-neon-auth-domain-to-redirect-uri-whitelist.md) | `POST /projects/:project_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/addneonauthdomaintoredirecturiwhitelist) |
| [Add a OAuth provider](actions/add-neon-auth-oauth-provider.md) | `POST /projects/:project_id/auth/oauth_providers` | [docs](https://api-docs.neon.tech/reference/addneonauthoauthprovider) |
| [Add JWKS URL](actions/add-project-jwks.md) | `POST /projects/:project_id/jwks` | [docs](https://api-docs.neon.tech/reference/addprojectjwks) |
| [Assign or update VPC endpoint](actions/assign-organization-vpc-endpoint.md) | `POST /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` | [docs](https://api-docs.neon.tech/reference/assignorganizationvpcendpoint) |
| [Set VPC endpoint restriction](actions/assign-project-vpc-endpoint.md) | `POST /projects/:project_id/vpc_endpoints/:vpc_endpoint_id` | [docs](https://api-docs.neon.tech/reference/assignprojectvpcendpoint) |
| [Retrieve number of branches](actions/count-project-branches.md) | `GET /projects/:project_id/branches/count` | [docs](https://api-docs.neon.tech/reference/countprojectbranches) |
| [Create API key](actions/create-api-key.md) | `POST /api_keys` | [docs](https://api-docs.neon.tech/reference/createapikey) |
| [Create new auth user](actions/create-branch-neon-auth-new-user.md) | `POST /projects/:project_id/branches/:branch_id/auth/users` | [docs](https://api-docs.neon.tech/reference/createbranchneonauthnewuser) |
| [Enable Neon Auth for the branch](actions/create-neon-auth.md) | `POST /projects/:project_id/branches/:branch_id/auth` | [docs](https://api-docs.neon.tech/reference/createneonauth) |
| [Create Neon Auth integration](actions/create-neon-auth-integration.md) | `POST /projects/auth/create` | [docs](https://api-docs.neon.tech/reference/createneonauthintegration) |
| [Create new auth user](actions/create-neon-auth-new-user.md) | `POST /projects/auth/user` | [docs](https://api-docs.neon.tech/reference/createneonauthnewuser) |
| [Create Auth Provider SDK keys](actions/create-neon-auth-provider-sdk-keys.md) | `POST /projects/auth/keys` | [docs](https://api-docs.neon.tech/reference/createneonauthprovidersdkkeys) |
| [Create organization API key](actions/create-org-api-key.md) | `POST /organizations/:org_id/api_keys` | [docs](https://api-docs.neon.tech/reference/createorgapikey) |
| [Create organization invitations](actions/create-organization-invitations.md) | `POST /organizations/:org_id/invitations` | [docs](https://api-docs.neon.tech/reference/createorganizationinvitations) |
| [Create project](actions/create-project.md) | `POST /projects` | [docs](https://api-docs.neon.tech/reference/createproject) |
| [Create branch](actions/create-project-branch.md) | `POST /projects/:project_id/branches` | [docs](https://api-docs.neon.tech/reference/createprojectbranch) |
| [Create anonymized branch](actions/create-project-branch-anonymized.md) | `POST /projects/:project_id/branch_anonymized` | [docs](https://api-docs.neon.tech/reference/createprojectbranchanonymized) |
| [Create Neon Data API](actions/create-project-branch-data-api.md) | `POST /projects/:project_id/branches/:branch_id/data-api/:database_name` | [docs](https://api-docs.neon.tech/reference/createprojectbranchdataapi) |
| [Create database](actions/create-project-branch-database.md) | `POST /projects/:project_id/branches/:branch_id/databases` | [docs](https://api-docs.neon.tech/reference/createprojectbranchdatabase) |
| [Create role](actions/create-project-branch-role.md) | `POST /projects/:project_id/branches/:branch_id/roles` | [docs](https://api-docs.neon.tech/reference/createprojectbranchrole) |
| [Create compute endpoint](actions/create-project-endpoint.md) | `POST /projects/:project_id/endpoints` | [docs](https://api-docs.neon.tech/reference/createprojectendpoint) |
| [Create a project transfer request](actions/create-project-transfer-request.md) | `POST /projects/:project_id/transfer_requests` | [docs](https://api-docs.neon.tech/reference/createprojecttransferrequest) |
| [Create snapshot](actions/create-snapshot.md) | `POST /projects/:project_id/branches/:branch_id/snapshot` | [docs](https://api-docs.neon.tech/reference/createsnapshot) |
| [Delete OAuth provider](actions/delete-branch-neon-auth-oauth-provider.md) | `DELETE /projects/:project_id/branches/:branch_id/auth/oauth_providers/:oauth_provider_id` | [docs](https://api-docs.neon.tech/reference/deletebranchneonauthoauthprovider) |
| [Delete domain from redirect_uri whitelist](actions/delete-branch-neon-auth-trusted-domain.md) | `DELETE /projects/:project_id/branches/:branch_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/deletebranchneonauthtrusteddomain) |
| [Delete auth user](actions/delete-branch-neon-auth-user.md) | `DELETE /projects/:project_id/branches/:branch_id/auth/users/:auth_user_id` | [docs](https://api-docs.neon.tech/reference/deletebranchneonauthuser) |
| [Delete domain from redirect_uri whitelist](actions/delete-neon-auth-domain-from-redirect-uri-whitelist.md) | `DELETE /projects/:project_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/deleteneonauthdomainfromredirecturiwhitelist) |
| [Delete integration with auth provider](actions/delete-neon-auth-integration.md) | `DELETE /projects/:project_id/auth/integration/:auth_provider` | [docs](https://api-docs.neon.tech/reference/deleteneonauthintegration) |
| [Delete OAuth provider](actions/delete-neon-auth-oauth-provider.md) | `DELETE /projects/:project_id/auth/oauth_providers/:oauth_provider_id` | [docs](https://api-docs.neon.tech/reference/deleteneonauthoauthprovider) |
| [Delete auth user](actions/delete-neon-auth-user.md) | `DELETE /projects/:project_id/auth/users/:auth_user_id` | [docs](https://api-docs.neon.tech/reference/deleteneonauthuser) |
| [Delete VPC endpoint](actions/delete-organization-vpc-endpoint.md) | `DELETE /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` | [docs](https://api-docs.neon.tech/reference/deleteorganizationvpcendpoint) |
| [Delete project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://api-docs.neon.tech/reference/deleteproject) |
| [Delete branch](actions/delete-project-branch.md) | `DELETE /projects/:project_id/branches/:branch_id` | [docs](https://api-docs.neon.tech/reference/deleteprojectbranch) |
| [Delete Neon Data API](actions/delete-project-branch-data-api.md) | `DELETE /projects/:project_id/branches/:branch_id/data-api/:database_name` | [docs](https://api-docs.neon.tech/reference/deleteprojectbranchdataapi) |
| [Delete database](actions/delete-project-branch-database.md) | `DELETE /projects/:project_id/branches/:branch_id/databases/:database_name` | [docs](https://api-docs.neon.tech/reference/deleteprojectbranchdatabase) |
| [Delete role](actions/delete-project-branch-role.md) | `DELETE /projects/:project_id/branches/:branch_id/roles/:role_name` | [docs](https://api-docs.neon.tech/reference/deleteprojectbranchrole) |
| [Delete compute endpoint](actions/delete-project-endpoint.md) | `DELETE /projects/:project_id/endpoints/:endpoint_id` | [docs](https://api-docs.neon.tech/reference/deleteprojectendpoint) |
| [Delete JWKS URL](actions/delete-project-jwks.md) | `DELETE /projects/:project_id/jwks/:jwks_id` | [docs](https://api-docs.neon.tech/reference/deleteprojectjwks) |
| [Delete VPC endpoint restriction](actions/delete-project-vpc-endpoint.md) | `DELETE /projects/:project_id/vpc_endpoints/:vpc_endpoint_id` | [docs](https://api-docs.neon.tech/reference/deleteprojectvpcendpoint) |
| [Delete snapshot](actions/delete-snapshot.md) | `DELETE /projects/:project_id/snapshots/:snapshot_id` | [docs](https://api-docs.neon.tech/reference/deletesnapshot) |
| [Disables Neon Auth for the branch](actions/disable-neon-auth.md) | `DELETE /projects/:project_id/branches/:branch_id/auth` | [docs](https://api-docs.neon.tech/reference/disableneonauth) |
| [Finalize restore](actions/finalize-restore-branch.md) | `POST /projects/:project_id/branches/:branch_id/finalize_restore` | [docs](https://api-docs.neon.tech/reference/finalizerestorebranch) |
| [List supported regions](actions/get-active-regions.md) | `GET /regions` | [docs](https://api-docs.neon.tech/reference/getactiveregions) |
| [Get anonymized branch status](actions/get-anonymized-branch-status.md) | `GET /projects/:project_id/branches/:branch_id/anonymized_status` | [docs](https://api-docs.neon.tech/reference/getanonymizedbranchstatus) |
| [Get request authentication details](actions/get-auth-details.md) | `GET /auth` | [docs](https://api-docs.neon.tech/reference/getauthdetails) |
| [Return available shared preload libraries](actions/get-available-preload-libraries.md) | `GET /projects/:project_id/available_preload_libraries` | [docs](https://api-docs.neon.tech/reference/getavailablepreloadlibraries) |
| [Retrieve connection URI](actions/get-connection-uri.md) | `GET /projects/:project_id/connection_uri` | [docs](https://api-docs.neon.tech/reference/getconnectionuri) |
| [Retrieve account consumption metrics (legacy plans)](actions/get-consumption-history-per-account.md) | `GET /consumption_history/account` | [docs](https://api-docs.neon.tech/reference/getconsumptionhistoryperaccount) |
| [Retrieve project consumption metrics (legacy plans)](actions/get-consumption-history-per-project.md) | `GET /consumption_history/projects` | [docs](https://api-docs.neon.tech/reference/getconsumptionhistoryperproject) |
| [Retrieve project consumption metrics](actions/get-consumption-history-per-project-v2.md) | `GET /consumption_history/v2/projects` | [docs](https://api-docs.neon.tech/reference/getconsumptionhistoryperprojectv2) |
| [Retrieve current user details](actions/get-current-user-info.md) | `GET /users/me` | [docs](https://api-docs.neon.tech/reference/getcurrentuserinfo) |
| [Retrieve current user organizations list](actions/get-current-user-organizations.md) | `GET /users/me/organizations` | [docs](https://api-docs.neon.tech/reference/getcurrentuserorganizations) |
| [Get masking rules](actions/get-masking-rules.md) | `GET /projects/:project_id/branches/:branch_id/masking_rules` | [docs](https://api-docs.neon.tech/reference/getmaskingrules) |
| [Get details of Neon Auth for the branch](actions/get-neon-auth.md) | `GET /projects/:project_id/branches/:branch_id/auth` | [docs](https://api-docs.neon.tech/reference/getneonauth) |
| [Get allow localhost](actions/get-neon-auth-allow-localhost.md) | `GET /projects/:project_id/branches/:branch_id/auth/allow_localhost` | [docs](https://api-docs.neon.tech/reference/getneonauthallowlocalhost) |
| [Get email and password configuration](actions/get-neon-auth-email-and-password-config.md) | `GET /projects/:project_id/branches/:branch_id/auth/email_and_password` | [docs](https://api-docs.neon.tech/reference/getneonauthemailandpasswordconfig) |
| [Get email provider configuration](actions/get-neon-auth-email-provider.md) | `GET /projects/:project_id/branches/:branch_id/auth/email_provider` | [docs](https://api-docs.neon.tech/reference/getneonauthemailprovider) |
| [Get email server configuration](actions/get-neon-auth-email-server.md) | `GET /projects/:project_id/auth/email_server` | [docs](https://api-docs.neon.tech/reference/getneonauthemailserver) |
| [Get all plugin configurations](actions/get-neon-auth-plugin-configs.md) | `GET /projects/:project_id/branches/:branch_id/auth/plugins` | [docs](https://api-docs.neon.tech/reference/getneonauthpluginconfigs) |
| [Get webhook configuration for Neon Auth](actions/get-neon-auth-webhook-config.md) | `GET /projects/:project_id/branches/:branch_id/auth/webhooks` | [docs](https://api-docs.neon.tech/reference/getneonauthwebhookconfig) |
| [Retrieve organization details](actions/get-organization.md) | `GET /organizations/:org_id` | [docs](https://api-docs.neon.tech/reference/getorganization) |
| [Retrieve organization invitation details](actions/get-organization-invitations.md) | `GET /organizations/:org_id/invitations` | [docs](https://api-docs.neon.tech/reference/getorganizationinvitations) |
| [Retrieve organization member details](actions/get-organization-member.md) | `GET /organizations/:org_id/members/:member_id` | [docs](https://api-docs.neon.tech/reference/getorganizationmember) |
| [Retrieve organization members details](actions/get-organization-members.md) | `GET /organizations/:org_id/members` | [docs](https://api-docs.neon.tech/reference/getorganizationmembers) |
| [Retrieve VPC endpoint details](actions/get-organization-vpc-endpoint-details.md) | `GET /organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id` | [docs](https://api-docs.neon.tech/reference/getorganizationvpcendpointdetails) |
| [Retrieve project details](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://api-docs.neon.tech/reference/getproject) |
| [Get advisor issues](actions/get-project-advisor-security-issues.md) | `GET /projects/:project_id/advisors` | [docs](https://api-docs.neon.tech/reference/getprojectadvisorsecurityissues) |
| [Retrieve branch details](actions/get-project-branch.md) | `GET /projects/:project_id/branches/:branch_id` | [docs](https://api-docs.neon.tech/reference/getprojectbranch) |
| [Get Neon Data API](actions/get-project-branch-data-api.md) | `GET /projects/:project_id/branches/:branch_id/data-api/:database_name` | [docs](https://api-docs.neon.tech/reference/getprojectbranchdataapi) |
| [Retrieve database details](actions/get-project-branch-database.md) | `GET /projects/:project_id/branches/:branch_id/databases/:database_name` | [docs](https://api-docs.neon.tech/reference/getprojectbranchdatabase) |
| [Retrieve role details](actions/get-project-branch-role.md) | `GET /projects/:project_id/branches/:branch_id/roles/:role_name` | [docs](https://api-docs.neon.tech/reference/getprojectbranchrole) |
| [Retrieve role password](actions/get-project-branch-role-password.md) | `GET /projects/:project_id/branches/:branch_id/roles/:role_name/reveal_password` | [docs](https://api-docs.neon.tech/reference/getprojectbranchrolepassword) |
| [Retrieve database schema](actions/get-project-branch-schema.md) | `GET /projects/:project_id/branches/:branch_id/schema` | [docs](https://api-docs.neon.tech/reference/getprojectbranchschema) |
| [Compare database schema](actions/get-project-branch-schema-comparison.md) | `GET /projects/:project_id/branches/:branch_id/compare_schema` | [docs](https://api-docs.neon.tech/reference/getprojectbranchschemacomparison) |
| [Retrieve compute endpoint details](actions/get-project-endpoint.md) | `GET /projects/:project_id/endpoints/:endpoint_id` | [docs](https://api-docs.neon.tech/reference/getprojectendpoint) |
| [List JWKS URLs](actions/get-project-jwks.md) | `GET /projects/:project_id/jwks` | [docs](https://api-docs.neon.tech/reference/getprojectjwks) |
| [Retrieve operation details](actions/get-project-operation.md) | `GET /projects/:project_id/operations/:operation_id` | [docs](https://api-docs.neon.tech/reference/getprojectoperation) |
| [View backup schedule](actions/get-snapshot-schedule.md) | `GET /projects/:project_id/branches/:branch_id/backup_schedule` | [docs](https://api-docs.neon.tech/reference/getsnapshotschedule) |
| [Grant project access](actions/grant-permission-to-project.md) | `POST /projects/:project_id/permissions` | [docs](https://api-docs.neon.tech/reference/grantpermissiontoproject) |
| [List API keys](actions/list-api-keys.md) | `GET /api_keys` | [docs](https://api-docs.neon.tech/reference/listapikeys) |
| [List OAuth providers for neon auth for a branch](actions/list-branch-neon-auth-oauth-providers.md) | `GET /projects/:project_id/branches/:branch_id/auth/oauth_providers` | [docs](https://api-docs.neon.tech/reference/listbranchneonauthoauthproviders) |
| [List domains in redirect_uri whitelist](actions/list-branch-neon-auth-trusted-domains.md) | `GET /projects/:project_id/branches/:branch_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/listbranchneonauthtrusteddomains) |
| [Lists active integrations with auth providers](actions/list-neon-auth-integrations.md) | `GET /projects/:project_id/auth/integrations` | [docs](https://api-docs.neon.tech/reference/listneonauthintegrations) |
| [List OAuth providers](actions/list-neon-auth-oauth-providers.md) | `GET /projects/:project_id/auth/oauth_providers` | [docs](https://api-docs.neon.tech/reference/listneonauthoauthproviders) |
| [List domains in redirect_uri whitelist](actions/list-neon-auth-redirect-uri-whitelist-domains.md) | `GET /projects/:project_id/auth/domains` | [docs](https://api-docs.neon.tech/reference/listneonauthredirecturiwhitelistdomains) |
| [List organization API keys](actions/list-org-api-keys.md) | `GET /organizations/:org_id/api_keys` | [docs](https://api-docs.neon.tech/reference/listorgapikeys) |
| [List VPC endpoints](actions/list-organization-vpc-endpoints.md) | `GET /organizations/:org_id/vpc/region/:region_id/vpc_endpoints` | [docs](https://api-docs.neon.tech/reference/listorganizationvpcendpoints) |
| [List VPC endpoints across all regions](actions/list-organization-vpc-endpoints-all-regions.md) | `GET /organizations/:org_id/vpc/vpc_endpoints` | [docs](https://api-docs.neon.tech/reference/listorganizationvpcendpointsallregions) |
| [List databases](actions/list-project-branch-databases.md) | `GET /projects/:project_id/branches/:branch_id/databases` | [docs](https://api-docs.neon.tech/reference/listprojectbranchdatabases) |
| [List branch endpoints](actions/list-project-branch-endpoints.md) | `GET /projects/:project_id/branches/:branch_id/endpoints` | [docs](https://api-docs.neon.tech/reference/listprojectbranchendpoints) |
| [List roles](actions/list-project-branch-roles.md) | `GET /projects/:project_id/branches/:branch_id/roles` | [docs](https://api-docs.neon.tech/reference/listprojectbranchroles) |
| [List branches](actions/list-project-branches.md) | `GET /projects/:project_id/branches` | [docs](https://api-docs.neon.tech/reference/listprojectbranches) |
| [List compute endpoints](actions/list-project-endpoints.md) | `GET /projects/:project_id/endpoints` | [docs](https://api-docs.neon.tech/reference/listprojectendpoints) |
| [List operations](actions/list-project-operations.md) | `GET /projects/:project_id/operations` | [docs](https://api-docs.neon.tech/reference/listprojectoperations) |
| [List project access](actions/list-project-permissions.md) | `GET /projects/:project_id/permissions` | [docs](https://api-docs.neon.tech/reference/listprojectpermissions) |
| [List VPC endpoint restrictions](actions/list-project-vpc-endpoints.md) | `GET /projects/:project_id/vpc_endpoints` | [docs](https://api-docs.neon.tech/reference/listprojectvpcendpoints) |
| [List projects](actions/list-projects.md) | `GET /projects` | [docs](https://api-docs.neon.tech/reference/listprojects) |
| [List shared projects](actions/list-shared-projects.md) | `GET /projects/shared` | [docs](https://api-docs.neon.tech/reference/listsharedprojects) |
| [List project snapshots](actions/list-snapshots.md) | `GET /projects/:project_id/snapshots` | [docs](https://api-docs.neon.tech/reference/listsnapshots) |
| [Recover a deleted project](actions/recover-project.md) | `POST /projects/:project_id/recover` | [docs](https://api-docs.neon.tech/reference/recoverproject) |
| [Remove member from the organization](actions/remove-organization-member.md) | `DELETE /organizations/:org_id/members/:member_id` | [docs](https://api-docs.neon.tech/reference/removeorganizationmember) |
| [Reset role password](actions/reset-project-branch-role-password.md) | `POST /projects/:project_id/branches/:branch_id/roles/:role_name/reset_password` | [docs](https://api-docs.neon.tech/reference/resetprojectbranchrolepassword) |
| [Restart compute endpoint](actions/restart-project-endpoint.md) | `POST /projects/:project_id/endpoints/:endpoint_id/restart` | [docs](https://api-docs.neon.tech/reference/restartprojectendpoint) |
| [Restore a deleted project](actions/restore-project.md) | `POST /projects/:project_id/restore` | [docs](https://api-docs.neon.tech/reference/restoreproject) |
| [Restore branch](actions/restore-project-branch.md) | `POST /projects/:project_id/branches/:branch_id/restore` | [docs](https://api-docs.neon.tech/reference/restoreprojectbranch) |
| [Restore snapshot](actions/restore-snapshot.md) | `POST /projects/:project_id/snapshots/:snapshot_id/restore` | [docs](https://api-docs.neon.tech/reference/restoresnapshot) |
| [Revoke API key](actions/revoke-api-key.md) | `DELETE /api_keys/:key_id` | [docs](https://api-docs.neon.tech/reference/revokeapikey) |
| [Revoke organization API key](actions/revoke-org-api-key.md) | `DELETE /organizations/:org_id/api_keys/:key_id` | [docs](https://api-docs.neon.tech/reference/revokeorgapikey) |
| [Revoke project access](actions/revoke-permission-from-project.md) | `DELETE /projects/:project_id/permissions/:permission_id` | [docs](https://api-docs.neon.tech/reference/revokepermissionfromproject) |
| [Send test email](actions/send-neon-auth-test-email.md) | `POST /projects/:project_id/branches/:branch_id/auth/send_test_email` | [docs](https://api-docs.neon.tech/reference/sendneonauthtestemail) |
| [Set branch as default](actions/set-default-project-branch.md) | `POST /projects/:project_id/branches/:branch_id/set_as_default` | [docs](https://api-docs.neon.tech/reference/setdefaultprojectbranch) |
| [Update backup schedule](actions/set-snapshot-schedule.md) | `PUT /projects/:project_id/branches/:branch_id/backup_schedule` | [docs](https://api-docs.neon.tech/reference/setsnapshotschedule) |
| [Start anonymization](actions/start-anonymization.md) | `POST /projects/:project_id/branches/:branch_id/anonymize` | [docs](https://api-docs.neon.tech/reference/startanonymization) |
| [Start compute endpoint](actions/start-project-endpoint.md) | `POST /projects/:project_id/endpoints/:endpoint_id/start` | [docs](https://api-docs.neon.tech/reference/startprojectendpoint) |
| [Suspend compute endpoint](actions/suspend-project-endpoint.md) | `POST /projects/:project_id/endpoints/:endpoint_id/suspend` | [docs](https://api-docs.neon.tech/reference/suspendprojectendpoint) |
| [Transfer Neon-managed auth project to your own account](actions/transfer-neon-auth-provider-project.md) | `POST /projects/auth/transfer_ownership` | [docs](https://api-docs.neon.tech/reference/transferneonauthproviderproject) |
| [Transfer projects between organizations](actions/transfer-projects-from-org-to-org.md) | `POST /organizations/:source_org_id/projects/transfer` | [docs](https://api-docs.neon.tech/reference/transferprojectsfromorgtoorg) |
| [Transfer projects from personal account to organization](actions/transfer-projects-from-user-to-org.md) | `POST /users/me/projects/transfer` | [docs](https://api-docs.neon.tech/reference/transferprojectsfromusertoorg) |
| [Update OAuth provider](actions/update-branch-neon-auth-oauth-provider.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/oauth_providers/:oauth_provider_id` | [docs](https://api-docs.neon.tech/reference/updatebranchneonauthoauthprovider) |
| [Update masking rules](actions/update-masking-rules.md) | `PATCH /projects/:project_id/branches/:branch_id/masking_rules` | [docs](https://api-docs.neon.tech/reference/updatemaskingrules) |
| [Update allow localhost](actions/update-neon-auth-allow-localhost.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/allow_localhost` | [docs](https://api-docs.neon.tech/reference/updateneonauthallowlocalhost) |
| [Update auth configuration](actions/update-neon-auth-config.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/config` | [docs](https://api-docs.neon.tech/reference/updateneonauthconfig) |
| [Update email and password configuration](actions/update-neon-auth-email-and-password-config.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/email_and_password` | [docs](https://api-docs.neon.tech/reference/updateneonauthemailandpasswordconfig) |
| [Update email provider configuration](actions/update-neon-auth-email-provider.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/email_provider` | [docs](https://api-docs.neon.tech/reference/updateneonauthemailprovider) |
| [Update email server configuration](actions/update-neon-auth-email-server.md) | `PATCH /projects/:project_id/auth/email_server` | [docs](https://api-docs.neon.tech/reference/updateneonauthemailserver) |
| [Update magic link plugin configuration](actions/update-neon-auth-magic-link-plugin.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/plugins/magic-link` | [docs](https://api-docs.neon.tech/reference/updateneonauthmagiclinkplugin) |
| [Update OAuth provider](actions/update-neon-auth-oauth-provider.md) | `PATCH /projects/:project_id/auth/oauth_providers/:oauth_provider_id` | [docs](https://api-docs.neon.tech/reference/updateneonauthoauthprovider) |
| [Update organization plugin configuration](actions/update-neon-auth-organization-plugin.md) | `PATCH /projects/:project_id/branches/:branch_id/auth/plugins/organization` | [docs](https://api-docs.neon.tech/reference/updateneonauthorganizationplugin) |
| [Update auth user role](actions/update-neon-auth-user-role.md) | `PUT /projects/:project_id/branches/:branch_id/auth/users/:auth_user_id/role` | [docs](https://api-docs.neon.tech/reference/updateneonauthuserrole) |
| [Update webhook configuration for Neon Auth](actions/update-neon-auth-webhook-config.md) | `PUT /projects/:project_id/branches/:branch_id/auth/webhooks` | [docs](https://api-docs.neon.tech/reference/updateneonauthwebhookconfig) |
| [Update role for organization member](actions/update-organization-member.md) | `PATCH /organizations/:org_id/members/:member_id` | [docs](https://api-docs.neon.tech/reference/updateorganizationmember) |
| [Update project](actions/update-project.md) | `PATCH /projects/:project_id` | [docs](https://api-docs.neon.tech/reference/updateproject) |
| [Update branch](actions/update-project-branch.md) | `PATCH /projects/:project_id/branches/:branch_id` | [docs](https://api-docs.neon.tech/reference/updateprojectbranch) |
| [Update Neon Data API](actions/update-project-branch-data-api.md) | `PATCH /projects/:project_id/branches/:branch_id/data-api/:database_name` | [docs](https://api-docs.neon.tech/reference/updateprojectbranchdataapi) |
| [Update database](actions/update-project-branch-database.md) | `PATCH /projects/:project_id/branches/:branch_id/databases/:database_name` | [docs](https://api-docs.neon.tech/reference/updateprojectbranchdatabase) |
| [Update compute endpoint](actions/update-project-endpoint.md) | `PATCH /projects/:project_id/endpoints/:endpoint_id` | [docs](https://api-docs.neon.tech/reference/updateprojectendpoint) |
| [Update snapshot](actions/update-snapshot.md) | `PATCH /projects/:project_id/snapshots/:snapshot_id` | [docs](https://api-docs.neon.tech/reference/updatesnapshot) |
