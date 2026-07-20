# <img src="https://images.mindcloud.co/apps/icons/neon-logomark-square_1776261963139.png" alt="Neon logo" width="28" height="28"> Neon: Universal API

Neon lets you manage serverless Postgres projects, branches, endpoints, organizations, snapshots, and Neon Auth resources through the official Neon API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neon/latest
- **Category:** IT Operations / Database
- **Actions:** 140
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://neon.tech
- **Vendor API docs:** https://api-docs.neon.tech/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve current user details](actions/get-current-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (140)

### A Pi Ke Y

| Action | Method | Description |
| --- | --- | --- |
| [Create API key](actions/create-api-key.md) | POST | Creates an API key in Neon. |
| [List API keys](actions/list-api-keys.md) | GET | Retrieves API keys from Neon. |
| [Revoke API key](actions/revoke-api-key.md) | DELETE | Revokes an API key from Neon. |

### A Pp Li Ca Ti On

| Action | Method | Description |
| --- | --- | --- |
| [Get request authentication details](actions/get-auth-details.md) | GET | Retrieves request authentication details from Neon. |

### B Ra Nc H

| Action | Method | Description |
| --- | --- | --- |
| [Add a OAuth provider](actions/add-branch-neon-auth-oauth-provider.md) | POST | Adds an OAuth provider in Neon. |
| [Add domain to redirect_uri whitelist](actions/add-branch-neon-auth-trusted-domain.md) | POST | Adds a domain to the redirect URI whitelist in Neon. |
| [Create new auth user](actions/create-branch-neon-auth-new-user.md) | POST | Creates an auth user in Neon. |
| [Enable Neon Auth for the branch](actions/create-neon-auth.md) | POST | Enables Neon Auth for a branch in Neon. |
| [Create branch](actions/create-project-branch.md) | POST | Creates a branch in Neon. |
| [Create anonymized branch](actions/create-project-branch-anonymized.md) | POST | Creates an anonymized branch in Neon. |
| [Create snapshot](actions/create-snapshot.md) | POST | Creates a snapshot in Neon. |
| [Delete OAuth provider](actions/delete-branch-neon-auth-oauth-provider.md) | DELETE | Deletes an OAuth provider from Neon. |
| [Delete domain from redirect_uri whitelist](actions/delete-branch-neon-auth-trusted-domain.md) | DELETE | Deletes a domain from the redirect URI whitelist in Neon. |
| [Delete auth user](actions/delete-branch-neon-auth-user.md) | DELETE | Deletes an auth user from Neon. |
| [Delete branch](actions/delete-project-branch.md) | DELETE | Deletes a branch from Neon. |
| [Disables Neon Auth for the branch](actions/disable-neon-auth.md) | DELETE | Disables Neon Auth for the branch in Neon. |
| [Finalize restore](actions/finalize-restore-branch.md) | POST | Finalizes branch restore from snapshot in Neon. |
| [Get anonymized branch status](actions/get-anonymized-branch-status.md) | GET | Retrieves anonymized branch status from Neon. |
| [Get masking rules](actions/get-masking-rules.md) | GET | Retrieves masking rules from Neon. |
| [Get details of Neon Auth for the branch](actions/get-neon-auth.md) | GET | Retrieves Neon Auth details for the branch from Neon. |
| [Get allow localhost](actions/get-neon-auth-allow-localhost.md) | GET | Retrieves localhost allow setting from Neon. |
| [Get email and password configuration](actions/get-neon-auth-email-and-password-config.md) | GET | Retrieves email and password configuration from Neon. |
| [Get email provider configuration](actions/get-neon-auth-email-provider.md) | GET | Retrieves email provider configuration from Neon. |
| [Get all plugin configurations](actions/get-neon-auth-plugin-configs.md) | GET | Retrieves Neon Auth plugin configurations from Neon. |
| [Get webhook configuration for Neon Auth](actions/get-neon-auth-webhook-config.md) | GET | Retrieves Neon Auth webhook configuration from Neon. |
| [Retrieve branch details](actions/get-project-branch.md) | GET | Retrieves branch details from Neon. |
| [Retrieve database schema](actions/get-project-branch-schema.md) | GET | Retrieves database schema from Neon. |
| [Compare database schema](actions/get-project-branch-schema-comparison.md) | GET | Compares database schemas in Neon. |
| [View backup schedule](actions/get-snapshot-schedule.md) | GET | Retrieves backup schedule from Neon. |
| [List OAuth providers for neon auth for a branch](actions/list-branch-neon-auth-oauth-providers.md) | GET | Retrieves OAuth providers for the branch from Neon. |
| [List domains in redirect_uri whitelist](actions/list-branch-neon-auth-trusted-domains.md) | GET | Retrieves redirect URI whitelist domains from Neon. |
| [List branches](actions/list-project-branches.md) | GET | Retrieves branches from Neon. |
| [Restore branch](actions/restore-project-branch.md) | POST | Restores branch to a historical state in Neon. |
| [Send test email](actions/send-neon-auth-test-email.md) | POST | Sends a test email in Neon. |
| [Set branch as default](actions/set-default-project-branch.md) | POST | Sets a branch as default in Neon. |
| [Update backup schedule](actions/set-snapshot-schedule.md) | PUT | Updates a backup schedule in Neon. |
| [Start anonymization](actions/start-anonymization.md) | POST | Starts anonymization for a branch in Neon. |
| [Update OAuth provider](actions/update-branch-neon-auth-oauth-provider.md) | PUT | Updates an OAuth provider in Neon. |
| [Update masking rules](actions/update-masking-rules.md) | PUT | Updates masking rules in Neon. |
| [Update allow localhost](actions/update-neon-auth-allow-localhost.md) | PUT | Updates localhost allow setting in Neon. |
| [Update auth configuration](actions/update-neon-auth-config.md) | PUT | Updates auth configuration in Neon. |
| [Update email and password configuration](actions/update-neon-auth-email-and-password-config.md) | PUT | Updates email and password configuration in Neon. |
| [Update email provider configuration](actions/update-neon-auth-email-provider.md) | PUT | Updates email provider configuration in Neon. |
| [Update magic link plugin configuration](actions/update-neon-auth-magic-link-plugin.md) | PUT | Updates magic link plugin configuration in Neon. |
| [Update organization plugin configuration](actions/update-neon-auth-organization-plugin.md) | PUT | Updates organization plugin configuration in Neon. |
| [Update auth user role](actions/update-neon-auth-user-role.md) | PUT | Updates an auth user role in Neon. |
| [Update webhook configuration for Neon Auth](actions/update-neon-auth-webhook-config.md) | PUT | Updates Neon Auth webhook configuration in Neon. |
| [Update branch](actions/update-project-branch.md) | PUT | Updates a branch in Neon. |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve number of branches](actions/count-project-branches.md) | GET | Retrieves the number of branches from Neon. |

### D At Ab As E

| Action | Method | Description |
| --- | --- | --- |
| [Create Neon Data API](actions/create-project-branch-data-api.md) | POST | Creates Neon Data API configuration in Neon. |
| [Create database](actions/create-project-branch-database.md) | POST | Creates a database in Neon. |
| [Delete Neon Data API](actions/delete-project-branch-data-api.md) | DELETE | Deletes Neon Data API configuration from Neon. |
| [Delete database](actions/delete-project-branch-database.md) | DELETE | Deletes a database from Neon. |
| [Get Neon Data API](actions/get-project-branch-data-api.md) | GET | Retrieves Neon Data API configuration from Neon. |
| [Retrieve database details](actions/get-project-branch-database.md) | GET | Retrieves database details from Neon. |
| [List databases](actions/list-project-branch-databases.md) | GET | Retrieves databases from Neon. |
| [Update Neon Data API](actions/update-project-branch-data-api.md) | PUT | Updates Neon Data API configuration in Neon. |
| [Update database](actions/update-project-branch-database.md) | PUT | Updates a database in Neon. |

### E Nd Po In T

| Action | Method | Description |
| --- | --- | --- |
| [Assign or update VPC endpoint](actions/assign-organization-vpc-endpoint.md) | POST | Assigns or updates VPC endpoint in Neon. |
| [Create compute endpoint](actions/create-project-endpoint.md) | POST | Creates a compute endpoint in Neon. |
| [Delete VPC endpoint](actions/delete-organization-vpc-endpoint.md) | DELETE | Deletes a VPC endpoint from Neon. |
| [Delete compute endpoint](actions/delete-project-endpoint.md) | DELETE | Deletes a compute endpoint from Neon. |
| [Retrieve VPC endpoint details](actions/get-organization-vpc-endpoint-details.md) | GET | Retrieves VPC endpoint details from Neon. |
| [Retrieve compute endpoint details](actions/get-project-endpoint.md) | GET | Retrieves compute endpoint details from Neon. |
| [List VPC endpoints](actions/list-organization-vpc-endpoints.md) | GET | Retrieves VPC endpoints from Neon. |
| [List VPC endpoints across all regions](actions/list-organization-vpc-endpoints-all-regions.md) | GET | Retrieves VPC endpoints across all regions from Neon. |
| [List branch endpoints](actions/list-project-branch-endpoints.md) | GET | Retrieves branch endpoints from Neon. |
| [List compute endpoints](actions/list-project-endpoints.md) | GET | Retrieves compute endpoints from Neon. |
| [Restart compute endpoint](actions/restart-project-endpoint.md) | POST | Restarts compute endpoint in Neon. |
| [Start compute endpoint](actions/start-project-endpoint.md) | POST | Starts compute endpoint in Neon. |
| [Suspend compute endpoint](actions/suspend-project-endpoint.md) | POST | Suspends compute endpoint in Neon. |
| [Update compute endpoint](actions/update-project-endpoint.md) | PUT | Updates a compute endpoint in Neon. |

### I Nv It At Io N

| Action | Method | Description |
| --- | --- | --- |
| [Create organization invitations](actions/create-organization-invitations.md) | POST | Creates organization invitations in Neon. |
| [Retrieve organization invitation details](actions/get-organization-invitations.md) | GET | Retrieves organization invitations from Neon. |

### J Ob

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve operation details](actions/get-project-operation.md) | GET | Retrieves operation details from Neon. |
| [List operations](actions/list-project-operations.md) | GET | Retrieves operations from Neon. |

### L Oc At Io N

| Action | Method | Description |
| --- | --- | --- |
| [List supported regions](actions/get-active-regions.md) | GET | Retrieves supported regions from Neon. |

### M Em Be Rs Hi P

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve organization member details](actions/get-organization-member.md) | GET | Retrieves organization member details from Neon. |
| [Retrieve organization members details](actions/get-organization-members.md) | GET | Retrieves organization members from Neon. |
| [Remove member from the organization](actions/remove-organization-member.md) | DELETE | Removes organization member from Neon. |
| [Update role for organization member](actions/update-organization-member.md) | PUT | Updates a role for organization member in Neon. |

### M Et Ri C

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve account consumption metrics (legacy plans)](actions/get-consumption-history-per-account.md) | GET |  |

### O Rg An Iz At Io N

| Action | Method | Description |
| --- | --- | --- |
| [Create organization API key](actions/create-org-api-key.md) | POST | Creates a organization API key in Neon. |
| [Retrieve current user organizations list](actions/get-current-user-organizations.md) | GET | Retrieves organizations for the current user from Neon. |
| [Retrieve organization details](actions/get-organization.md) | GET | Retrieves organization details from Neon. |
| [List organization API keys](actions/list-org-api-keys.md) | GET | Retrieves organization API keys from Neon. |
| [Revoke organization API key](actions/revoke-org-api-key.md) | DELETE | Revokes a organization API key from Neon. |
| [Transfer projects between organizations](actions/transfer-projects-from-org-to-org.md) | POST | Transfers projects between organizations in Neon. |

### P Er Mi Ss Io N

| Action | Method | Description |
| --- | --- | --- |
| [Grant project access](actions/grant-permission-to-project.md) | POST | Grants project access in Neon. |
| [List project access](actions/list-project-permissions.md) | GET | Retrieves project access from Neon. |
| [Revoke project access](actions/revoke-permission-from-project.md) | DELETE | Revokes a project access from Neon. |

### P Ro Je Ct

| Action | Method | Description |
| --- | --- | --- |
| [Accept a project transfer request](actions/accept-project-transfer-request.md) | PUT | Accepts a project transfer request in Neon. |
| [Add domain to redirect_uri whitelist](actions/add-neon-auth-domain-to-redirect-uri-whitelist.md) | POST | Adds trusted redirect URI domain in Neon. |
| [Add a OAuth provider](actions/add-neon-auth-oauth-provider.md) | POST | Adds an OAuth provider in Neon. |
| [Add JWKS URL](actions/add-project-jwks.md) | POST | Adds a JWKS URL to a project in Neon. |
| [Set VPC endpoint restriction](actions/assign-project-vpc-endpoint.md) | POST | Sets a VPC endpoint restriction in Neon. |
| [Create Neon Auth integration](actions/create-neon-auth-integration.md) | POST | Creates Neon Auth integration in Neon. |
| [Create new auth user](actions/create-neon-auth-new-user.md) | POST | Creates an auth user in Neon. |
| [Create Auth Provider SDK keys](actions/create-neon-auth-provider-sdk-keys.md) | POST | Creates auth provider SDK keys in Neon. |
| [Create project](actions/create-project.md) | POST | Creates a project in Neon. |
| [Create a project transfer request](actions/create-project-transfer-request.md) | POST | Creates a project transfer request in Neon. |
| [Delete domain from redirect_uri whitelist](actions/delete-neon-auth-domain-from-redirect-uri-whitelist.md) | DELETE | Deletes trusted redirect URI domain from Neon. |
| [Delete integration with auth provider](actions/delete-neon-auth-integration.md) | DELETE | Deletes an auth provider integration from Neon. |
| [Delete OAuth provider](actions/delete-neon-auth-oauth-provider.md) | DELETE | Deletes an OAuth provider from Neon. |
| [Delete auth user](actions/delete-neon-auth-user.md) | DELETE | Deletes an auth user from Neon. |
| [Delete project](actions/delete-project.md) | DELETE | Deletes a project from Neon. |
| [Delete JWKS URL](actions/delete-project-jwks.md) | DELETE | Deletes a JWKS URL from a project in Neon. |
| [Delete VPC endpoint restriction](actions/delete-project-vpc-endpoint.md) | DELETE | Deletes a VPC endpoint restriction from Neon. |
| [Delete snapshot](actions/delete-snapshot.md) | DELETE | Deletes a snapshot from Neon. |
| [Return available shared preload libraries](actions/get-available-preload-libraries.md) | GET | Retrieves available shared preload libraries from Neon. |
| [Retrieve connection URI](actions/get-connection-uri.md) | GET | Retrieves a connection URI from Neon. |
| [Retrieve project consumption metrics (legacy plans)](actions/get-consumption-history-per-project.md) | GET | Retrieves project consumption metrics from Neon. |
| [Retrieve project consumption metrics](actions/get-consumption-history-per-project-v2.md) | GET | Retrieves project consumption metrics from Neon. |
| [Get email server configuration](actions/get-neon-auth-email-server.md) | GET | Retrieves email server configuration from Neon. |
| [Retrieve project details](actions/get-project.md) | GET | Retrieves project details from Neon. |
| [Get advisor issues](actions/get-project-advisor-security-issues.md) | GET | Retrieves advisor issues for a project from Neon. |
| [List JWKS URLs](actions/get-project-jwks.md) | GET | Retrieves JWKS URLs for a project from Neon. |
| [Lists active integrations with auth providers](actions/list-neon-auth-integrations.md) | GET | Retrieves active integrations with auth providers from Neon. |
| [List OAuth providers](actions/list-neon-auth-oauth-providers.md) | GET | Retrieves OAuth providers from Neon. |
| [List domains in redirect_uri whitelist](actions/list-neon-auth-redirect-uri-whitelist-domains.md) | GET | Retrieves trusted redirect URI domains from Neon. |
| [List VPC endpoint restrictions](actions/list-project-vpc-endpoints.md) | GET | Retrieves VPC endpoint restrictions from Neon. |
| [List projects](actions/list-projects.md) | GET | Retrieves projects from Neon. |
| [List shared projects](actions/list-shared-projects.md) | GET | Retrieves shared projects from Neon. |
| [List project snapshots](actions/list-snapshots.md) | GET | Retrieves project snapshots from Neon. |
| [Recover a deleted project](actions/recover-project.md) | POST | Recovers a deleted project in Neon. |
| [Restore a deleted project](actions/restore-project.md) | POST |  |
| [Restore snapshot](actions/restore-snapshot.md) | POST | Restores snapshot in Neon. |
| [Transfer Neon-managed auth project to your own account](actions/transfer-neon-auth-provider-project.md) | POST | Transfers Neon-managed auth project to your own account in Neon. |
| [Transfer projects from personal account to organization](actions/transfer-projects-from-user-to-org.md) | POST | Transfers projects to an organization in Neon. |
| [Update email server configuration](actions/update-neon-auth-email-server.md) | PUT | Updates email server configuration in Neon. |
| [Update OAuth provider](actions/update-neon-auth-oauth-provider.md) | PUT | Updates an OAuth provider in Neon. |
| [Update project](actions/update-project.md) | PUT | Updates a project in Neon. |
| [Update snapshot](actions/update-snapshot.md) | PUT | Updates a snapshot in Neon. |

### R Ol E

| Action | Method | Description |
| --- | --- | --- |
| [Create role](actions/create-project-branch-role.md) | POST | Creates a role in Neon. |
| [Delete role](actions/delete-project-branch-role.md) | DELETE | Deletes a role from Neon. |
| [Retrieve role details](actions/get-project-branch-role.md) | GET | Retrieves role details from Neon. |
| [Retrieve role password](actions/get-project-branch-role-password.md) | GET | Retrieves a role password from Neon. |
| [List roles](actions/list-project-branch-roles.md) | GET | Retrieves roles from Neon. |
| [Reset role password](actions/reset-project-branch-role-password.md) | POST | Resets a role password in Neon. |

### U Se R

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve current user details](actions/get-current-user-info.md) | GET | Retrieves current user details from Neon. |

