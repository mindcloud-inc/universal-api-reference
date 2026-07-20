# Acronis: Native API Reference

A consolidated summary of Acronis's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.acronis.com/doc/outbound/apis/index.html
- **API base URL:** `{dataCenterUrl}`

## Authentication

### OAuth2 Client Credentials

Use an Acronis API client ID, client secret, and data center URL to exchange a bearer token.

### Credentials

- **Data Center URL:** `dataCenterUrl` · required · The Acronis data center base URL for your tenant, for example https://eu2-cloud.acronis.com.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.dataCenterUrl}}/api/2/idp/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.acronis.com/doc/outbound/apis/authentication/authentication.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Protection Plan To Resources](actions/apply-protection-plan-to-resources.md) | `POST /api/policy_management/v4/applications` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/applying-plan-to-resources.html) |
| [Change Tenant Quotas](actions/change-tenant-quotas.md) | `PUT /api/2/tenants/{tenant_id}/offering_items` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/changing-quotas.html) |
| [Check User Login Availability](actions/check-user-login-availability.md) | `GET /api/2/users/check_login` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/creating-user.html) |
| [Create Protection Plan](actions/create-protection-plan.md) | `POST /api/policy_management/v4/policies` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/creating-protection-plan.html) |
| [Create Tenant](actions/create-tenant.md) | `POST /api/2/tenants` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/creating-tenant.html) |
| [Create User](actions/create-user.md) | `POST /api/2/user` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/creating-user.html) |
| [Delete Protection Plan](actions/delete-protection-plan.md) | `DELETE /api/policy_management/v4/policies/{policy_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/deleting-plan.html) |
| [Delete Tenant](actions/delete-tenant.md) | `DELETE /api/2/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/deleting-tenant.html) |
| [Delete User](actions/delete-user.md) | `DELETE /api/2/users/{user_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/deleting-user.html) |
| [Disable Service For Sub-Tenant](actions/disable-service-for-sub-tenant.md) | `DELETE /api/2/applications/{application_id}/bindings/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/disabling-service.html) |
| [Disable Tenant](actions/disable-tenant.md) | `PUT /api/2/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/disabling-tenant.html) |
| [Enable Service For Sub-Tenant](actions/enable-service-for-sub-tenant.md) | `POST /api/2/applications/{application_id}/bindings/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/enabling-service.html) |
| [Get Resource Details](actions/get-resource-details.md) | `GET /api/resource_management/v4/resources/{resource_id}/attributes` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resource-info.html) |
| [Get Resource Protection Status](actions/get-resource-protection-status.md) | `GET /api/resource_management/v4/resource_statuses` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-protection-status-of-resources.html) |
| [Get Service](actions/get-service.md) | `GET /api/2/applications/{application_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/fetching-service.html) |
| [Get Tenant](actions/get-tenant.md) | `GET /api/2/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-tenant.html) |
| [Get Tenant Production Start Date](actions/get-tenant-production-start-date.md) | `GET /api/2/tenants/{tenant_id}/pricing` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-tenant-prod-date.html) |
| [Get User](actions/get-user.md) | `GET /api/2/users/{user_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/fetching-user-info.html) |
| [Get User Access Policies](actions/get-user-access-policies.md) | `GET /api/2/users/{user_id}/access_policies` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/roles/check.html) |
| [List Applicable Plans For Resource](actions/list-applicable-plans-for-resource.md) | `GET /api/policy_management/v4/policies` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/fetching-applicable-plans-for-resource.html) |
| [List Child Tenants](actions/list-child-tenants.md) | `GET /api/2/tenants/{tenant_id}/children` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-child-tenants.html) |
| [List Platform Services](actions/list-platform-services.md) | `GET /api/2/applications` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/fetching-all-services.html) |
| [List Protection Plans](actions/list-protection-plans.md) | `GET /api/policy_management/v4/policies` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/fetching-plans-policies.html) |
| [List Resources](actions/list-resources.md) | `GET /api/resource_management/v4/resources` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resources.html) |
| [List Resources By Type](actions/list-resources-by-type.md) | `GET /api/resource_management/v4/resources` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resources-by-type.html) |
| [List Tasks](actions/list-tasks.md) | `GET /api/task_manager/v2/tasks` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/tasks/tasks/fetching-tasks.html) |
| [List Tenant Offering Items](actions/list-tenant-offering-items.md) | `GET /api/2/tenants/{tenant_id}/offering_items` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/fetching-available-ois.html) |
| [List Tenant Services](actions/list-tenant-services.md) | `GET /api/2/tenants/{tenant_id}/applications` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/fetching-services.html) |
| [List Tenants](actions/list-tenants.md) | `GET /api/2/tenants` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-tenants.html) |
| [Revoke Protection Plans From Resources](actions/revoke-protection-plans-from-resources.md) | `DELETE /api/policy_management/v4/applications` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/revoking-plan-from-resources.html) |
| [Search Resources](actions/search-resources.md) | `GET /api/resource_management/v4/resources` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resources-using-search.html) |
| [Send User Activation Email](actions/send-user-activation-email.md) | `POST /api/2/users/{user_id}/send-activation-email` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/activation/email.html) |
| [Set User Password](actions/set-user-password.md) | `POST /api/2/users/{user_id}/password` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/activation/password.html) |
| [Start Policy Execution](actions/start-policy-execution.md) | `PUT /api/policy_management/v4/applications/run` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/starting-policy.html) |
| [Switch Tenant Service Edition](actions/switch-tenant-service-edition.md) | `PUT /api/2/tenants/{tenant_id}/edition` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/switching-edition.html) |
| [Toggle Tenant Offering Item](actions/toggle-tenant-offering-item.md) | `PUT /api/2/tenants/{tenant_id}/offering_items` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/enabling-disabling-ois.html) |
| [Update Protection Plan](actions/update-protection-plan.md) | `PATCH /api/policy_management/v4/policies/{policy_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/updating-policy-or-plan.html) |
| [Update Tenant](actions/update-tenant.md) | `PUT /api/2/tenants/{tenant_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/modifying-tenant.html) |
| [Update User Access Policies](actions/update-user-access-policies.md) | `PUT /api/2/users/{user_id}/access_policies` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/roles/modify.html) |
| [Update User Email](actions/update-user-email.md) | `PUT /api/2/users/{user_id}` | [docs](https://developer.acronis.com/doc/outbound/apis/api-library/account/users/changing-email.html) |
