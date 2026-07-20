# <img src="https://images.mindcloud.co/apps/icons/mekari-qontak_1776957706942.png" alt="Mekari Qontak logo" width="28" height="28"> Mekari Qontak: Universal API

Qontak CRM wrapper for Mekari's HMAC-signed CRM API surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mekariQontak/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 86
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qontak.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/22728681/2sAXxV6A5V

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact Fields](actions/get-contact-template.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-contact-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (86)

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [Apply Approval Rules](actions/apply-approval-rules.md) | PUT | Applies approval rules in Mekari Qontak. |
| [List Approval Rules](actions/get-approval-rules.md) | GET | Retrieves approval rules from Mekari Qontak. |
| [Toggle Approval Workflow](actions/toggle-approval-workflow.md) | PUT | Toggles a parallel approval workflow in Mekari Qontak. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Mekari Qontak. |
| [Create Company Without Validation](actions/create-company-novalidate.md) | POST | Creates a company in Mekari Qontak without validation. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Mekari Qontak. |
| [List Companies](actions/get-all-companies.md) | GET | Retrieves companies from Mekari Qontak. |
| [Get Company](actions/get-company-by-id.md) | GET | Retrieves a company from Mekari Qontak. |
| [Get Company Fields](actions/get-company-template.md) | GET | Retrieves company fields from Mekari Qontak. |
| [Get Company Timeline](actions/get-company-timeline.md) | GET | Retrieves a company timeline from Mekari Qontak. |
| [Update Company Without Validation](actions/update-company-novalidate.md) | PUT | Updates a company in Mekari Qontak without validation. |
| [Update Company Owner](actions/update-company-owner.md) | PUT | Updates a company owner in Mekari Qontak. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Mekari Qontak. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Mekari Qontak. |
| [List Contacts](actions/get-all-contacts.md) | GET | Retrieves contacts from Mekari Qontak. |
| [List Contacts by Date](actions/get-all-contacts-date-search.md) | GET | Finds contacts in Mekari Qontak using date filters. |
| [Get Contact Chat History](actions/get-contact-chat-history.md) | GET | Retrieves contact chat history from Mekari Qontak. |
| [Get Contact Fields](actions/get-contact-template.md) | GET | Retrieves contact fields from Mekari Qontak. |
| [Get Contact Timeline](actions/get-contact-timeline.md) | GET | Retrieves a contact timeline from Mekari Qontak. |
| [Get Contact](actions/get-single-contact.md) | GET | Retrieves a contact from Mekari Qontak. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Mekari Qontak. |
| [Update Contact Owner](actions/update-contact-owner.md) | PUT | Updates a contact owner in Mekari Qontak. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Auto Assign Deal](actions/auto-assign-deal.md) | PUT | Automatically assigns deals in Mekari Qontak. |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Mekari Qontak. |
| [Update Deal Permissions](actions/deal-permission.md) | PUT | Updates deal permissions in Mekari Qontak. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Mekari Qontak. |
| [List Deal Full Fields](actions/get-all-deal-full-fields.md) | GET | Retrieves all full deal fields from Mekari Qontak. |
| [List Deals](actions/get-all-deals.md) | GET | Retrieves deals from Mekari Qontak. |
| [Get Deal by Channel Integration Room ID](actions/get-deal-by-channel-integration-room-id.md) | GET | Retrieves a deal by channel integration room ID in Mekari Qontak. |
| [Get Deal Change Log](actions/get-deal-change-log.md) | GET | Retrieves a deal change log from Mekari Qontak. |
| [Get Deal Chat History](actions/get-deal-chat-history.md) | GET | Retrieves deal chat history from Mekari Qontak. |
| [Get Deal Full Fields](actions/get-deal-full-field.md) | GET | Retrieves full deal fields from Mekari Qontak. |
| [Get Deal Creator](actions/get-deal-real-creator.md) | GET | Retrieves a deal creator from Mekari Qontak. |
| [Get Deal SLA](actions/get-deal-sla.md) | GET | Retrieves deal SLA details from Mekari Qontak. |
| [Get Deal Stage History](actions/get-deal-stage-history.md) | GET | Retrieves deal stage history from Mekari Qontak. |
| [Get Deal Fields](actions/get-deal-template.md) | GET | Retrieves deal fields from Mekari Qontak. |
| [Get Deal Timeline](actions/get-deal-timeline.md) | GET | Retrieves a deal timeline from Mekari Qontak. |
| [Get Deal](actions/get-single-deal.md) | GET | Retrieves a deal from Mekari Qontak. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Mekari Qontak. |
| [Update Deal Attributes](actions/update-deal-attribute.md) | PUT | Updates deal attributes in Mekari Qontak. |
| [Update Deal Owner](actions/update-deal-owner.md) | PUT | Updates a deal owner in Mekari Qontak. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Geolocation](actions/create-geolocation.md) | POST | Creates a new geolocation in Mekari Qontak. |
| [List Geolocations](actions/get-all-geolocations.md) | GET | Retrieves geolocations from Mekari Qontak. |
| [Get Geolocation](actions/get-geolocation-by-id.md) | GET | Retrieves a geolocation from Mekari Qontak. |
| [Update Geolocation](actions/update-geolocation.md) | PUT | Updates an existing geolocation in Mekari Qontak. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Mekari Qontak. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from Mekari Qontak. |
| [List Notes](actions/get-all-notes.md) | GET | Retrieves notes from Mekari Qontak. |
| [Get Note](actions/get-note-by-id.md) | GET | Retrieves a note from Mekari Qontak. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in Mekari Qontak. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification](actions/create-notification.md) | POST | Sends a notification in Mekari Qontak. |
| [List Notifications](actions/get-all-notifications.md) | GET | Retrieves notifications from Mekari Qontak. |
| [Get Notification](actions/get-notification-by-id.md) | GET | Retrieves a notification from Mekari Qontak. |
| [Get Notification Fields](actions/get-notification-template.md) | GET | Retrieves notification fields from Mekari Qontak. |
| [Mark All Notifications as Read](actions/mark-all-notifications-as-read.md) | PUT | Marks all notifications as read in Mekari Qontak. |
| [Mark Notification as Read](actions/mark-notification-as-read.md) | PUT | Marks a notification as read in Mekari Qontak. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/get-all-pipelines.md) | GET | Retrieves pipelines from Mekari Qontak. |
| [Get Pipeline](actions/get-single-pipeline.md) | GET | Retrieves a pipeline from Mekari Qontak. |
| [List Pipeline Stages](actions/get-stages-from-pipeline.md) | GET | Retrieves pipeline stages from Mekari Qontak. |

### Product Association

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Association](actions/create-product-association.md) | POST | Creates a product association in Mekari Qontak. |
| [Delete Product Association](actions/delete-product-association.md) | DELETE | Deletes a product association from Mekari Qontak. |
| [List Product Associations](actions/get-all-product-associations.md) | GET | Retrieves product associations from Mekari Qontak. |
| [Get Product Association](actions/get-product-association-by-id.md) | GET | Retrieves a product association from Mekari Qontak. |
| [Update Product Association](actions/update-product-association.md) | PUT | Updates a product association in Mekari Qontak. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Mekari Qontak. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Mekari Qontak. |
| [List Products](actions/get-all-products.md) | GET | Retrieves products from Mekari Qontak. |
| [Get Product](actions/get-product-by-id.md) | GET | Retrieves a product from Mekari Qontak. |
| [Get Product Fields](actions/get-product-template.md) | GET | Retrieves product fields from Mekari Qontak. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Mekari Qontak. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Category](actions/add-task-category.md) | POST | Creates a task category in Mekari Qontak. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Mekari Qontak. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Mekari Qontak. |
| [Delete Task Category](actions/delete-task-category.md) | DELETE | Deletes a task category from Mekari Qontak. |
| [List Tasks](actions/get-all-tasks.md) | GET | Retrieves tasks from Mekari Qontak. |
| [Get Task](actions/get-task-by-id.md) | GET | Retrieves a task from Mekari Qontak. |
| [List Task Categories](actions/get-task-category.md) | GET | Retrieves task categories from Mekari Qontak. |
| [Get Task Fields](actions/get-task-template.md) | GET | Retrieves task fields from Mekari Qontak. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Mekari Qontak. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Mekari Qontak. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from Mekari Qontak. |
| [List Tickets](actions/get-all-tickets.md) | GET | Retrieves tickets from Mekari Qontak. |
| [Get Ticket](actions/get-single-ticket.md) | GET | Retrieves a ticket from Mekari Qontak. |
| [List Ticket Pipelines](actions/get-ticket-pipelines.md) | GET | Retrieves ticket pipelines from Mekari Qontak. |
| [Get Ticket Fields](actions/get-ticket-template.md) | GET | Retrieves ticket fields from Mekari Qontak. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Mekari Qontak. |

