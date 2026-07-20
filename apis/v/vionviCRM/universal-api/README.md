# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-24-as-13_1777046635319.png" alt="vionvi CRM logo" width="28" height="28"> vionvi CRM: Universal API

vionvi CRM is a tenant-scoped CRM API for managing clients, leads, contracts, tasks, organizations, funnels, sources, payments, realty objects, catalogs, users, and related operational records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vionviCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://280-crm.vionvi.com
- **Vendor API docs:** https://280-crm-api.vionvi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Show Current User](actions/show-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Catalog Items](actions/list-catalog-items.md) | GET | Retrieves catalog items from vionvi CRM. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from vionvi CRM. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from vionvi CRM. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from vionvi CRM. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from vionvi CRM. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from vionvi CRM. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from vionvi CRM. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Count Clients](actions/count-clients.md) | GET | Retrieves the client count from vionvi CRM. |
| [Count Contracts](actions/count-contracts.md) | GET | Retrieves the contract count from vionvi CRM. |
| [Count Leads](actions/count-leads.md) | GET | Retrieves the lead count from vionvi CRM. |
| [Count Payments](actions/count-payments.md) | GET | Retrieves the payment count from vionvi CRM. |
| [Count Tasks](actions/count-tasks.md) | GET | Retrieves the task count from vionvi CRM. |
| [Count Users](actions/count-users.md) | GET | Retrieves the user count from vionvi CRM. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from vionvi CRM. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from vionvi CRM. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves permissions from vionvi CRM. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Funnels](actions/list-funnels.md) | GET | Retrieves funnels from vionvi CRM. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from vionvi CRM. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from vionvi CRM. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves services from vionvi CRM. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Task Statuses](actions/list-task-statuses.md) | GET | Retrieves task statuses from vionvi CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from vionvi CRM. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from vionvi CRM. |
| [Show Current User](actions/show-current-user.md) | GET | Retrieves the current user from vionvi CRM. |

