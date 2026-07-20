# <img src="https://images.mindcloud.co/apps/icons/easybill_1775166245574.png" alt="easybill logo" width="28" height="28"> easybill: Universal API

Manage easybill customers, contacts, documents, payments, products, projects, tasks, templates, inventory, and webhooks through the official easybill REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easybill/latest
- **Category:** Commerce / Accounting
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easybill.de/
- **Vendor API docs:** https://www.easybill.de/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybill/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an attachment from easybill by ID. |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from easybill. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from easybill by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from easybill. |

### Discounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Position Discount](actions/get-position-discount.md) | GET | Retrieves a position discount from easybill by ID. |
| [Get Position Group Discount](actions/get-position-group-discount.md) | GET | Retrieves a position group discount from easybill by ID. |
| [List Position Discounts](actions/list-position-discounts.md) | GET | Retrieves position discounts from easybill. |
| [List Position Group Discounts](actions/list-position-group-discounts.md) | GET | Retrieves position group discounts from easybill. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from easybill by ID. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from easybill. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Position](actions/get-position.md) | GET | Retrieves a position from easybill by ID. |
| [List Positions](actions/list-positions.md) | GET | Retrieves positions from easybill. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from easybill by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from easybill. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from easybill by ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from easybill. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Text Template](actions/get-text-template.md) | GET | Retrieves a text template from easybill by ID. |
| [List PDF Templates](actions/list-pdf-templates.md) | GET | Retrieves PDF templates from easybill. |
| [List Text Templates](actions/list-text-templates.md) | GET | Retrieves text templates from easybill. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Position Group](actions/get-position-group.md) | GET | Retrieves a position group from easybill by ID. |
| [Get Post Box](actions/get-post-box.md) | GET | Retrieves a post box from easybill by ID. |
| [Get Serial Number](actions/get-serial-number.md) | GET | Retrieves a serial number from easybill by ID. |
| [Get Stock](actions/get-stock.md) | GET | Retrieves a stock entry from easybill by ID. |
| [Get Time Tracking](actions/get-time-tracking.md) | GET | Retrieves a time tracking from easybill by ID. |
| [List Position Groups](actions/list-position-groups.md) | GET | Retrieves position groups from easybill. |
| [List Post Boxes](actions/list-post-boxes.md) | GET | Retrieves post boxes from easybill. |
| [List Serial Numbers](actions/list-serial-numbers.md) | GET | Retrieves serial numbers from easybill. |
| [List Stocks](actions/list-stocks.md) | GET | Retrieves stock entries from easybill. |
| [List Time Trackings](actions/list-time-trackings.md) | GET | Retrieves time trackings from easybill. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Login](actions/get-login.md) | GET | Retrieves a login from easybill by ID. |
| [List Logins](actions/list-logins.md) | GET | Retrieves logins from easybill. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get WebHook](actions/get-web-hook.md) | GET | Retrieves a webhook from easybill by ID. |
| [List WebHooks](actions/list-web-hooks.md) | GET | Retrieves webhooks from easybill. |

