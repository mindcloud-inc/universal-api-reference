# <img src="https://images.mindcloud.co/apps/icons/help-space_1775823400690.png" alt="HelpSpace logo" width="28" height="28"> HelpSpace: Universal API

HelpSpace is a customer support platform API for tickets, ticket messages, customers, scrum tasks, knowledge-base docs, tags, reports, and webhook configuration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helpSpace/latest
- **Category:** Support / Ticketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mindcloudstage0.helpspace.com
- **Vendor API docs:** https://documentation.helpspace.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tickets](actions/list-tickets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment Media](actions/get-attachment-media.md) | GET | Retrieves attachment media from HelpSpace. |

### Channels Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Channels Report](actions/get-channels-report.md) | GET | Retrieves a channels report from HelpSpace. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in HelpSpace. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes a customer from HelpSpace. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from HelpSpace. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from HelpSpace. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in HelpSpace. |

### Customer Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Avatar](actions/get-customer-avatar.md) | GET | Retrieves a customer avatar from HelpSpace. |
| [Update Customer Avatar](actions/update-customer-avatar.md) | PUT | Updates a customer avatar in HelpSpace. |

### Docs Article

| Action | Method | Description |
| --- | --- | --- |
| [Get Docs Article](actions/get-docs-article.md) | GET | Retrieves a docs article from HelpSpace. |
| [List Docs Articles](actions/list-docs-articles.md) | GET | Retrieves docs articles from HelpSpace. |

### Docs Category

| Action | Method | Description |
| --- | --- | --- |
| [List Docs Categories](actions/list-docs-categories.md) | GET | Retrieves docs categories from HelpSpace. |

### Docs Site

| Action | Method | Description |
| --- | --- | --- |
| [List Docs Sites](actions/list-docs-sites.md) | GET | Retrieves docs sites from HelpSpace. |

### Inline Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Inline Media](actions/get-inline-media.md) | GET | Retrieves inline media from HelpSpace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Message](actions/create-ticket-message.md) | POST | Creates a ticket message in HelpSpace. |
| [Get Ticket Message](actions/get-ticket-message.md) | GET | Retrieves a ticket message from HelpSpace. |
| [List Ticket Messages](actions/list-ticket-messages.md) | GET | Retrieves messages for a HelpSpace ticket. |

### Performance Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Performance Report](actions/get-performance-report.md) | GET | Retrieves a performance report from HelpSpace. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in HelpSpace. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from HelpSpace. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from HelpSpace. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from HelpSpace. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in HelpSpace. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in HelpSpace. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from HelpSpace. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from HelpSpace. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from HelpSpace. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in HelpSpace. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in HelpSpace. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes a ticket from HelpSpace. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from HelpSpace. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from HelpSpace. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in HelpSpace. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves the webhook from HelpSpace. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates the webhook in HelpSpace. |

### Webhook Log

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Logs](actions/list-webhook-logs.md) | GET | Retrieves webhook logs from HelpSpace. |

