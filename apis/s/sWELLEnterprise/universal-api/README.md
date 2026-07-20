# <img src="https://images.mindcloud.co/apps/icons/s-wellenterprise_1776270137455.png" alt="SWELLEnterprise logo" width="28" height="28"> SWELLEnterprise: Universal API

Manage CRM, billing, projects, forms, and client portals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sWELLEnterprise/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://swellsystem.com
- **Vendor API docs:** https://dashboard.swellsystem.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Portal Configuration](actions/get-portal-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in SWELLEnterprise. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | POST | Creates multiple contacts in SWELLEnterprise. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in SWELLEnterprise. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in SWELLEnterprise. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in SWELLEnterprise. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in SWELLEnterprise. |

### Portal Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Configuration](actions/get-portal-configuration.md) | GET | Retrieves portal configuration from SWELLEnterprise. |

### Portal Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Invite Company To Portal](actions/invite-company-to-portal.md) | POST | Sends a portal invitation to a company in SWELLEnterprise. |
| [Invite Contact To Portal](actions/invite-contact-to-portal.md) | POST | Sends a portal invitation to a contact in SWELLEnterprise. |

### Portal Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Token](actions/get-portal-token.md) | GET | Retrieves a portal token from SWELLEnterprise. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in SWELLEnterprise. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in SWELLEnterprise. |

### Project Approval

| Action | Method | Description |
| --- | --- | --- |
| [Approve Project Approval](actions/approve-project-approval.md) | PUT | Approves a project approval in SWELLEnterprise. |
| [Create Project Approval](actions/create-project-approval.md) | POST | Creates a project approval in SWELLEnterprise. |
| [Reject Project Approval](actions/reject-project-approval.md) | PUT | Rejects a project approval in SWELLEnterprise. |
| [Request Changes On Project Approval](actions/request-changes-on-project-approval.md) | PUT | Requests changes on a project approval in SWELLEnterprise. |

### Revision Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Revision Request](actions/create-revision-request.md) | POST | Creates a revision request in SWELLEnterprise. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in SWELLEnterprise. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in SWELLEnterprise. |
| [Regenerate Webhook Secret](actions/regenerate-webhook-secret.md) | PUT | Regenerates a webhook secret in SWELLEnterprise. |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT | Updates a webhook subscription in SWELLEnterprise. |

