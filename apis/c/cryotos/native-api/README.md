# Cryotos: Native API Reference

A consolidated summary of Cryotos's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.cryotos.com/documentation
- **API base URL:** `https://app.cryotos.com`

## Authentication

### Email & Password (JWT)

Sign in to Cryotos with an account email and password. MindCloud exchanges that login for a JWT bearer token and uses it for later API requests.

### Credentials

- **Username:** `username` · required · Cryotos account email used to sign in to the Cryotos web app.

Send these headers with each API request:

```http
Authorization: Bearer <custom.id_token>
```

[Official authentication documentation](https://www.cryotos.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /api/authenticate` | [docs](https://www.cryotos.com/documentation) |
| [Get Current Organization](actions/get-current-organization.md) | `GET /api/organizations/getCurrentOrganizations` | [docs](https://www.cryotos.com/documentation) |
| [Get Current User](actions/get-current-user.md) | `GET /api/account` | [docs](https://www.cryotos.com/documentation) |
| [Get Email Template](actions/get-email-template.md) | `GET /api/email_template/:id` | [docs](https://www.cryotos.com/cmms/features/email-and-whatsapp-builder) |
| [Get Template](actions/get-template.md) | `GET /api/templates/:id` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [Get Workflow Template Category Counts By Type](actions/get-workflow-template-category-counts-by-type.md) | `GET /api/publicTemplateCategories/template-count/list-by-type/:type` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [List Aisles](actions/list-aisles.md) | `GET /api/aisles` | [docs](https://www.cryotos.com/cmms/features/warehouse-management) |
| [List Bin Locations](actions/list-bin-locations.md) | `GET /api/bin-locations` | [docs](https://www.cryotos.com/cmms/features/warehouse-management) |
| [List Bins](actions/list-bins.md) | `GET /api/bins` | [docs](https://www.cryotos.com/cmms/features/warehouse-management) |
| [List Email Broadcast Schedules](actions/list-email-broadcast-schedules.md) | `GET /api/email-broadcast-schedule` | [docs](https://www.cryotos.com/cmms/features/email-and-whatsapp-builder) |
| [List Email Templates](actions/list-email-templates.md) | `GET /api/email_template` | [docs](https://www.cryotos.com/cmms/features/email-and-whatsapp-builder) |
| [List Public Templates](actions/list-public-templates.md) | `GET /api/publictemplates` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [List Racks](actions/list-racks.md) | `GET /api/racks` | [docs](https://www.cryotos.com/cmms/features/warehouse-management) |
| [List Requests](actions/list-requests.md) | `GET /api/requests` | [docs](https://www.cryotos.com/cmms/features/work-requests) |
| [List Shelves](actions/list-shelves.md) | `GET /api/selves` | [docs](https://www.cryotos.com/cmms/features/warehouse-management) |
| [List Template Histories By Workflow ID](actions/list-template-histories-by-workflow-id.md) | `GET /api/template-histories/findByWorkflowId/:workflowId` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [List Templates](actions/list-templates.md) | `GET /api/templates` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [List Workflow Template Categories](actions/list-workflow-template-categories.md) | `GET /api/publicTemplateCategories` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
| [Search Email Templates](actions/search-email-templates.md) | `GET /api/dropdown/emailTemplate/_autocomplete/:text` | [docs](https://www.cryotos.com/cmms/features/email-and-whatsapp-builder) |
| [Search Workflow Template Categories](actions/search-workflow-template-categories.md) | `GET /api/publicTemplateCategories/_search/:text` | [docs](https://www.cryotos.com/cmms/features/workflow-automation-software) |
