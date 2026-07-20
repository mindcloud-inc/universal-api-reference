# <img src="https://images.mindcloud.co/apps/icons/acronis_1777386807541.png" alt="Acronis logo" width="28" height="28"> Acronis: Universal API

Manage Acronis Cyber Protect Cloud tenants, services, users, resources, protection plans, tasks, and events through the official Acronis platform APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/acronis/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.acronis.com/
- **Vendor API docs:** https://developer.acronis.com/doc/outbound/apis/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tenants](actions/list-tenants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Offering Item

| Action | Method | Description |
| --- | --- | --- |
| [Change Tenant Quotas](actions/change-tenant-quotas.md) | PUT | Updates tenant offering item quotas in Acronis. |
| [List Tenant Offering Items](actions/list-tenant-offering-items.md) | GET | Retrieves available offering items for a tenant in Acronis. |
| [Switch Tenant Service Edition](actions/switch-tenant-service-edition.md) | PUT | Switches a tenant service edition in Acronis. |
| [Toggle Tenant Offering Item](actions/toggle-tenant-offering-item.md) | PUT | Enables or disables a tenant offering item in Acronis. |

### Protection Plan

| Action | Method | Description |
| --- | --- | --- |
| [Apply Protection Plan To Resources](actions/apply-protection-plan-to-resources.md) | PUT | Applies a protection plan to resources in Acronis. |
| [Create Protection Plan](actions/create-protection-plan.md) | POST | Creates a new protection plan in Acronis. |
| [Delete Protection Plan](actions/delete-protection-plan.md) | DELETE | Deletes an existing protection plan from Acronis. |
| [List Applicable Plans For Resource](actions/list-applicable-plans-for-resource.md) | GET | Retrieves protection plans applicable to a resource in Acronis. |
| [List Protection Plans](actions/list-protection-plans.md) | GET | Retrieves protection plans and policies from Acronis. |
| [Revoke Protection Plans From Resources](actions/revoke-protection-plans-from-resources.md) | PUT | Revokes protection plans from resources in Acronis. |
| [Start Policy Execution](actions/start-policy-execution.md) | PUT | Starts execution of a protection policy in Acronis. |
| [Update Protection Plan](actions/update-protection-plan.md) | PUT | Updates an existing protection plan in Acronis. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Details](actions/get-resource-details.md) | GET | Retrieves detailed information about a resource from Acronis. |
| [List Resources](actions/list-resources.md) | GET | Retrieves a list of resources from Acronis. |
| [List Resources By Type](actions/list-resources-by-type.md) | GET | Retrieves resources by type from Acronis. |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in Acronis by search expression. |

### Resource Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Protection Status](actions/get-resource-protection-status.md) | GET | Retrieves protection statuses for resources from Acronis. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from Acronis. |
| [List Platform Services](actions/list-platform-services.md) | GET | Retrieves all platform services from Acronis. |
| [List Tenant Services](actions/list-tenant-services.md) | GET | Retrieves services enabled for a tenant in Acronis. |

### Service Binding

| Action | Method | Description |
| --- | --- | --- |
| [Disable Service For Sub-Tenant](actions/disable-service-for-sub-tenant.md) | DELETE | Disables a service for a sub-tenant in Acronis. |
| [Enable Service For Sub-Tenant](actions/enable-service-for-sub-tenant.md) | POST | Enables a service for a sub-tenant in Acronis. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Acronis. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Create Tenant](actions/create-tenant.md) | POST | Creates a new tenant in Acronis. |
| [Delete Tenant](actions/delete-tenant.md) | DELETE | Deletes an existing tenant from Acronis. |
| [Disable Tenant](actions/disable-tenant.md) | PUT | Disables an existing tenant in Acronis. |
| [Get Tenant](actions/get-tenant.md) | GET | Retrieves a tenant from Acronis. |
| [List Child Tenants](actions/list-child-tenants.md) | GET | Retrieves child tenants for a tenant in Acronis. |
| [List Tenants](actions/list-tenants.md) | GET | Retrieves a list of tenants from Acronis. |
| [Update Tenant](actions/update-tenant.md) | PUT | Updates an existing tenant in Acronis. |

### Tenant Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Production Start Date](actions/get-tenant-production-start-date.md) | GET | Retrieves a tenant's production start date from Acronis. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Check User Login Availability](actions/check-user-login-availability.md) | GET | Checks whether a user login is available in Acronis. |
| [Create User](actions/create-user.md) | POST | Creates a new user account in Acronis. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user account from Acronis. |
| [Get User](actions/get-user.md) | GET | Retrieves a user account from Acronis. |
| [Update User Email](actions/update-user-email.md) | PUT | Updates a user's email address in Acronis. |

### User Access Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get User Access Policies](actions/get-user-access-policies.md) | GET | Retrieves access policies for a user in Acronis. |
| [Update User Access Policies](actions/update-user-access-policies.md) | PUT | Updates access policies for a user in Acronis. |

### User Activation

| Action | Method | Description |
| --- | --- | --- |
| [Send User Activation Email](actions/send-user-activation-email.md) | POST | Sends a user activation email from Acronis. |
| [Set User Password](actions/set-user-password.md) | PUT | Sets a user's password to activate the account in Acronis. |

