# Sonderplan: Native API Reference

A consolidated summary of Sonderplan's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://docs.sonderplan.com/api-reference
- **API base URL:** `https://api.sonderplan.com/v2`

## Authentication

### Bearer Token

Use a Sonderplan API Client bearer token. The platform will send it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sonderplan.com/en/admin/api-clients)

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Bookings](actions/bulk-bookings.md) | `POST /booking/bulk` | [docs](https://docs.sonderplan.com/api-reference/booking/bulk-bookings) |
| [Create Billable Item](actions/create-billable-item.md) | `POST /billable-item` | [docs](https://docs.sonderplan.com/api-reference/billable-item/create-billable-item) |
| [Create Booking](actions/create-booking.md) | `POST /booking` | [docs](https://docs.sonderplan.com/api-reference/booking/create-booking) |
| [Create Calendar Subscription](actions/create-calendar-subscription.md) | `POST /calendar-subscription/import` | [docs](https://docs.sonderplan.com/api-reference/calendar-subscription/create-calendar-subscription) |
| [Create Contact](actions/create-contact.md) | `POST /contact` | [docs](https://docs.sonderplan.com/api-reference/contact/create-contact) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom-field` | [docs](https://docs.sonderplan.com/api-reference/custom-field/create-custom-field) |
| [Create Group](actions/create-group.md) | `POST /group` | [docs](https://docs.sonderplan.com/api-reference/group/create-group) |
| [Create Invoice Template](actions/create-invoice-template.md) | `POST /invoice-template` | [docs](https://docs.sonderplan.com/api-reference/invoice-template/create-invoice-template) |
| [Delete Billable Item](actions/delete-billable-item.md) | `DELETE /billable-item` | [docs](https://docs.sonderplan.com/api-reference/billable-item/delete-billable-item) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /booking` | [docs](https://docs.sonderplan.com/api-reference/booking/delete-booking) |
| [Delete Calendar Subscription](actions/delete-calendar-subscription.md) | `DELETE /calendar-subscription/import` | [docs](https://docs.sonderplan.com/api-reference/calendar-subscription/delete-calendar-subscription) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact` | [docs](https://docs.sonderplan.com/api-reference/contact/delete-contact) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom-field` | [docs](https://docs.sonderplan.com/api-reference/custom-field/delete-custom-field) |
| [Delete Group](actions/delete-group.md) | `DELETE /group` | [docs](https://docs.sonderplan.com/api-reference/group/delete-group) |
| [Delete Invoice Template](actions/delete-invoice-template.md) | `DELETE /invoice-template` | [docs](https://docs.sonderplan.com/api-reference/invoice-template/delete-invoice-template) |
| [Duplicate Invoice](actions/duplicate-invoice.md) | `POST /invoice/duplicate` | [docs](https://docs.sonderplan.com/api-reference/invoice/duplicate-invoice) |
| [Duplicate Quote](actions/duplicate-quote.md) | `POST /quote/duplicate` | [docs](https://docs.sonderplan.com/api-reference/quote/duplicate-quote) |
| [Generate Invoice PDF](actions/generate-invoice-pdf.md) | `GET /invoice/pdf` | [docs](https://docs.sonderplan.com/api-reference/invoice/generate-invoice-pdf) |
| [Generate Quote PDF](actions/generate-quote-pdf.md) | `GET /quote/pdf` | [docs](https://docs.sonderplan.com/api-reference/quote/generate-quote-pdf) |
| [Get Billable Items](actions/get-billable-items.md) | `GET /billable-item` | [docs](https://docs.sonderplan.com/api-reference/billable-item/get-billable-items) |
| [Get Booking Clashes](actions/get-booking-clashes.md) | `GET /booking/checkclash` | [docs](https://docs.sonderplan.com/api-reference/booking/get-booking-clashes) |
| [Get Bookings](actions/get-bookings.md) | `GET /booking` | [docs](https://docs.sonderplan.com/api-reference/booking/get-bookings) |
| [Get Calendar Subscriptions](actions/get-calendar-subscriptions.md) | `GET /calendar-subscription/import` | [docs](https://docs.sonderplan.com/api-reference/calendar-subscription/get-calendar-subscriptions) |
| [Get Contacts](actions/get-contacts.md) | `GET /contact` | [docs](https://docs.sonderplan.com/api-reference/contact/get-contacts) |
| [Get Custom Fields](actions/get-custom-fields.md) | `GET /custom-field` | [docs](https://docs.sonderplan.com/api-reference/custom-field/get-custom-fields) |
| [Get Groups](actions/get-groups.md) | `GET /group` | [docs](https://docs.sonderplan.com/api-reference/group/get-groups) |
| [Get Instance](actions/get-instance.md) | `GET /instance` | [docs](https://docs.sonderplan.com/api-reference/instance/get-instance) |
| [Get Invoice Templates](actions/get-invoice-templates.md) | `GET /invoice-template` | [docs](https://docs.sonderplan.com/api-reference/invoice-template/get-invoice-templates) |
| [Get Invoices](actions/get-invoices.md) | `GET /invoice` | [docs](https://docs.sonderplan.com/api-reference/invoice/get-invoices) |
| [Get Project Folders](actions/get-project-folders.md) | `GET /project/folder` | [docs](https://docs.sonderplan.com/api-reference/project/get-project-folders) |
| [Get Project Phases](actions/get-project-phases.md) | `GET /project/phase` | [docs](https://docs.sonderplan.com/api-reference/project/get-project-phases) |
| [Get Projects](actions/get-projects.md) | `GET /project` | [docs](https://docs.sonderplan.com/api-reference/project/get-projects) |
| [Get Quotes](actions/get-quotes.md) | `GET /quote` | [docs](https://docs.sonderplan.com/api-reference/quote/get-quotes) |
| [Get Rate Schemes](actions/get-rate-schemes.md) | `GET /rate-scheme` | [docs](https://docs.sonderplan.com/api-reference/rate-scheme/get-rate-schemes) |
| [Get Resources](actions/get-resources.md) | `GET /resource` | [docs](https://docs.sonderplan.com/api-reference/resource/get-resources) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://docs.sonderplan.com/api-reference/status/get-status) |
| [Get Taxes](actions/get-taxes.md) | `GET /tax` | [docs](https://docs.sonderplan.com/api-reference/tax/get-taxes) |
| [Get Time Activities](actions/get-time-activities.md) | `GET /time-activity` | [docs](https://docs.sonderplan.com/api-reference/time-activity/get-time-activities) |
| [Get Time Entries](actions/get-time-entries.md) | `GET /time-entry` | [docs](https://docs.sonderplan.com/api-reference/time-entry/get-time-entries) |
| [Get Users](actions/get-users.md) | `GET /user` | [docs](https://docs.sonderplan.com/api-reference/user/get-users) |
| [Get Workspaces](actions/get-workspaces.md) | `GET /workspace` | [docs](https://docs.sonderplan.com/api-reference/workspace/get-workspaces) |
| [Lock Booking](actions/lock-booking.md) | `PUT /booking/lock` | [docs](https://docs.sonderplan.com/api-reference/booking/lock-booking) |
| [Stop Time Entry](actions/stop-time-entry.md) | `PATCH /time-entry/stop` | [docs](https://docs.sonderplan.com/api-reference/time-entry/stop-time-entry) |
| [Unlock Booking](actions/unlock-booking.md) | `PUT /booking/unlock` | [docs](https://docs.sonderplan.com/api-reference/booking/unlock-booking) |
| [Update Billable Item](actions/update-billable-item.md) | `PUT /billable-item` | [docs](https://docs.sonderplan.com/api-reference/billable-item/update-billable-item) |
| [Update Booking](actions/update-booking.md) | `PUT /booking` | [docs](https://docs.sonderplan.com/api-reference/booking/update-booking) |
| [Update Calendar Subscription](actions/update-calendar-subscription.md) | `PUT /calendar-subscription/import` | [docs](https://docs.sonderplan.com/api-reference/calendar-subscription/update-calendar-subscription) |
| [Update Contact](actions/update-contact.md) | `PUT /contact` | [docs](https://docs.sonderplan.com/api-reference/contact/update-contact) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /custom-field` | [docs](https://docs.sonderplan.com/api-reference/custom-field/update-custom-field) |
| [Update Group](actions/update-group.md) | `PUT /group` | [docs](https://docs.sonderplan.com/api-reference/group/update-group) |
| [Update Invoice Template](actions/update-invoice-template.md) | `PUT /invoice-template` | [docs](https://docs.sonderplan.com/api-reference/invoice-template/update-invoice-template) |
