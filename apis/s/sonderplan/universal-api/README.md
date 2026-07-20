# <img src="https://images.mindcloud.co/apps/icons/sonderplan-icon_1776107535841.png" alt="Sonderplan logo" width="28" height="28"> Sonderplan: Universal API

Sonderplan is an online resource scheduling platform for managing rooms, equipment, people, projects, quotes, invoices, and time tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sonderplan/latest
- **Category:** Productivity / Scheduling
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sonderplan.com
- **Vendor API docs:** https://docs.sonderplan.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Instance](actions/get-instance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Billable Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Billable Item](actions/create-billable-item.md) | POST |  |
| [Delete Billable Item](actions/delete-billable-item.md) | DELETE |  |
| [Get Billable Items](actions/get-billable-items.md) | GET |  |
| [Update Billable Item](actions/update-billable-item.md) | PUT |  |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST |  |
| [Delete Booking](actions/delete-booking.md) | DELETE |  |
| [Get Bookings](actions/get-bookings.md) | GET |  |
| [Lock Booking](actions/lock-booking.md) | PUT |  |
| [Unlock Booking](actions/unlock-booking.md) | PUT |  |
| [Update Booking](actions/update-booking.md) | PUT |  |

### Booking Batch

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Bookings](actions/bulk-bookings.md) | POST |  |

### Booking Clash

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Clashes](actions/get-booking-clashes.md) | GET |  |

### Calendar Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Subscription](actions/create-calendar-subscription.md) | POST |  |
| [Delete Calendar Subscription](actions/delete-calendar-subscription.md) | DELETE |  |
| [Get Calendar Subscriptions](actions/get-calendar-subscriptions.md) | GET |  |
| [Update Calendar Subscription](actions/update-calendar-subscription.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contacts](actions/get-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE |  |
| [Get Custom Fields](actions/get-custom-fields.md) | GET |  |
| [Update Custom Field](actions/update-custom-field.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Groups](actions/get-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Instance

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance](actions/get-instance.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Invoice](actions/duplicate-invoice.md) | POST |  |
| [Get Invoices](actions/get-invoices.md) | GET |  |

### Invoice Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate Invoice PDF](actions/generate-invoice-pdf.md) | GET |  |

### Invoice Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice Template](actions/create-invoice-template.md) | POST |  |
| [Delete Invoice Template](actions/delete-invoice-template.md) | DELETE |  |
| [Get Invoice Templates](actions/get-invoice-templates.md) | GET |  |
| [Update Invoice Template](actions/update-invoice-template.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Projects](actions/get-projects.md) | GET |  |

### Project Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Folders](actions/get-project-folders.md) | GET |  |

### Project Phase

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Phases](actions/get-project-phases.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Quote](actions/duplicate-quote.md) | POST |  |
| [Get Quotes](actions/get-quotes.md) | GET |  |

### Quote Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate Quote PDF](actions/generate-quote-pdf.md) | GET |  |

### Rate Scheme

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate Schemes](actions/get-rate-schemes.md) | GET |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resources](actions/get-resources.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status](actions/get-status.md) | GET |  |

### Tax

| Action | Method | Description |
| --- | --- | --- |
| [Get Taxes](actions/get-taxes.md) | GET |  |

### Time Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Activities](actions/get-time-activities.md) | GET |  |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entries](actions/get-time-entries.md) | GET |  |
| [Stop Time Entry](actions/stop-time-entry.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspaces](actions/get-workspaces.md) | GET |  |

