# Mekari Qontak: Native API Reference

A consolidated summary of Mekari Qontak's API configuration and 86 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/22728681/2sAXxV6A5V
- **API base URL:** `https://api.mekari.com`

## Authentication

### HMAC

HMAC-signed credentials for the Mekari Qontak CRM API.

### Credentials

- **Client ID:** `clientId` · required · Mekari HMAC client ID for the Qontak CRM application.
- **Client Secret:** `clientSecret` · required · Mekari HMAC client secret for the Qontak CRM application.
- **CRM User SSO ID:** `crmUserSsoId` · required · Qontak CRM user SSO ID sent in the X-Crm-User-Sso-Id header for requests.

[Official authentication documentation](https://developers.mekari.com/docs/kb/hmac-authentication)

## API conventions

Response data is read from `response`.

## Endpoints (86 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task Category](actions/add-task-category.md) | `POST qontak/crm/tasks/category` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Apply Approval Rules](actions/apply-approval-rules.md) | `POST qontak/crm/approvals/apply_rules` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Auto Assign Deal](actions/auto-assign-deal.md) | `POST qontak/crm/deals/auto-assign` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Company](actions/create-company.md) | `POST qontak/crm/companies` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Company Without Validation](actions/create-company-novalidate.md) | `POST qontak/crm/companies` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Contact](actions/create-contact.md) | `POST qontak/crm/contacts` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Deal](actions/create-deal.md) | `POST qontak/crm/deals` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Geolocation](actions/create-geolocation.md) | `POST qontak/crm/geolocations` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Note](actions/create-note.md) | `POST qontak/crm/notes` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Send Notification](actions/create-notification.md) | `POST qontak/crm/notifications` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Product](actions/create-product.md) | `POST qontak/crm/products` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Product Association](actions/create-product-association.md) | `POST qontak/crm/products_association` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Task](actions/create-task.md) | `POST qontak/crm/tasks` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Create Ticket](actions/create-ticket.md) | `POST qontak/crm/tickets` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Deal Permissions](actions/deal-permission.md) | `POST qontak/crm/deals/deal_permission` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Company](actions/delete-company.md) | `DELETE qontak/crm/companies/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Contact](actions/delete-contact.md) | `DELETE qontak/crm/contacts/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Deal](actions/delete-deal.md) | `DELETE qontak/crm/deals/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Note](actions/delete-note.md) | `DELETE qontak/crm/notes/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Product](actions/delete-product.md) | `DELETE qontak/crm/products/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Product Association](actions/delete-product-association.md) | `DELETE qontak/crm/products_association/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Task](actions/delete-task.md) | `DELETE qontak/crm/tasks/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Task Category](actions/delete-task-category.md) | `DELETE qontak/crm/tasks/category/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE qontak/crm/tickets/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Companies](actions/get-all-companies.md) | `GET qontak/crm/companies` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Contacts](actions/get-all-contacts.md) | `GET qontak/crm/contacts` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Contacts by Date](actions/get-all-contacts-date-search.md) | `GET qontak/crm/contacts` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Deal Full Fields](actions/get-all-deal-full-fields.md) | `GET qontak/crm/deals/full-fields` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Deals](actions/get-all-deals.md) | `GET qontak/crm/deals` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Geolocations](actions/get-all-geolocations.md) | `GET qontak/crm/geolocations` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Notes](actions/get-all-notes.md) | `GET qontak/crm/notes` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Notifications](actions/get-all-notifications.md) | `GET qontak/crm/notifications` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Pipelines](actions/get-all-pipelines.md) | `GET qontak/crm/pipelines` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Product Associations](actions/get-all-product-associations.md) | `GET qontak/crm/products_association` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Products](actions/get-all-products.md) | `GET qontak/crm/products` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Tasks](actions/get-all-tasks.md) | `GET qontak/crm/tasks` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Tickets](actions/get-all-tickets.md) | `GET qontak/crm/tickets` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Approval Rules](actions/get-approval-rules.md) | `GET qontak/crm/approvals/rules` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Company](actions/get-company-by-id.md) | `GET qontak/crm/companies/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Company Fields](actions/get-company-template.md) | `GET qontak/crm/companies/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Company Timeline](actions/get-company-timeline.md) | `GET qontak/crm/companies/:id/timeline` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Contact Chat History](actions/get-contact-chat-history.md) | `GET qontak/crm/contacts/:id/chat-history` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Contact Fields](actions/get-contact-template.md) | `GET qontak/crm/contacts/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Contact Timeline](actions/get-contact-timeline.md) | `GET qontak/crm/contacts/:id/timeline` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal by Channel Integration Room ID](actions/get-deal-by-channel-integration-room-id.md) | `GET qontak/crm/deals/channel_integration_room/:channel_integration_room_id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Change Log](actions/get-deal-change-log.md) | `GET qontak/crm/deals/:id/change_log` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Chat History](actions/get-deal-chat-history.md) | `GET qontak/crm/deals/:id/chat-history` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Full Fields](actions/get-deal-full-field.md) | `GET qontak/crm/deals/:id/full-field` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Creator](actions/get-deal-real-creator.md) | `GET qontak/crm/deals/:id/real_creator` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal SLA](actions/get-deal-sla.md) | `GET qontak/crm/deals/sla` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Stage History](actions/get-deal-stage-history.md) | `GET qontak/crm/deals/:id/stage_history` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Fields](actions/get-deal-template.md) | `GET qontak/crm/deals/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal Timeline](actions/get-deal-timeline.md) | `GET qontak/crm/deals/:id/timeline` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Geolocation](actions/get-geolocation-by-id.md) | `GET qontak/crm/geolocations/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Note](actions/get-note-by-id.md) | `GET qontak/crm/notes/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Notification](actions/get-notification-by-id.md) | `GET qontak/crm/notifications/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Notification Fields](actions/get-notification-template.md) | `GET qontak/crm/notifications/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Product Association](actions/get-product-association-by-id.md) | `GET qontak/crm/products_association/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Product](actions/get-product-by-id.md) | `GET qontak/crm/products/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Product Fields](actions/get-product-template.md) | `GET qontak/crm/products/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Contact](actions/get-single-contact.md) | `GET qontak/crm/contacts/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Deal](actions/get-single-deal.md) | `GET qontak/crm/deals/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Pipeline](actions/get-single-pipeline.md) | `GET qontak/crm/pipelines/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Ticket](actions/get-single-ticket.md) | `GET qontak/crm/tickets/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Pipeline Stages](actions/get-stages-from-pipeline.md) | `GET qontak/crm/pipelines/:id/stages` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Task](actions/get-task-by-id.md) | `GET qontak/crm/tasks/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Task Categories](actions/get-task-category.md) | `GET qontak/crm/tasks/category` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Task Fields](actions/get-task-template.md) | `GET qontak/crm/tasks/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [List Ticket Pipelines](actions/get-ticket-pipelines.md) | `GET qontak/crm/tickets/ticket_pipelines` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Get Ticket Fields](actions/get-ticket-template.md) | `GET qontak/crm/tickets/info` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Mark All Notifications as Read](actions/mark-all-notifications-as-read.md) | `PUT qontak/crm/notifications/mark_all_as_read` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Mark Notification as Read](actions/mark-notification-as-read.md) | `PUT qontak/crm/notifications/:id/mark_as_read` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Toggle Approval Workflow](actions/toggle-approval-workflow.md) | `POST qontak/crm/approvals/toggle_workflow` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Company Without Validation](actions/update-company-novalidate.md) | `PUT qontak/crm/companies/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Company Owner](actions/update-company-owner.md) | `PUT qontak/crm/companies/:id/update_owner` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Contact](actions/update-contact.md) | `PUT qontak/crm/contacts/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Contact Owner](actions/update-contact-owner.md) | `PUT qontak/crm/contacts/:id/update_owner` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Deal](actions/update-deal.md) | `PUT qontak/crm/deals/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Deal Attributes](actions/update-deal-attribute.md) | `POST qontak/crm/deals/update_attribute` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Deal Owner](actions/update-deal-owner.md) | `PUT qontak/crm/deals/:id/update_owner` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Geolocation](actions/update-geolocation.md) | `PUT qontak/crm/geolocations/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Note](actions/update-note.md) | `PUT qontak/crm/notes/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Product](actions/update-product.md) | `PUT qontak/crm/products/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Product Association](actions/update-product-association.md) | `PUT qontak/crm/products_association/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Task](actions/update-task.md) | `PUT qontak/crm/tasks/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
| [Update Ticket](actions/update-ticket.md) | `PUT qontak/crm/tickets/:id` | [docs](https://documenter.getpostman.com/view/22728681/2sAXxV6A5V) |
