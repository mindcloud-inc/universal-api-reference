# <img src="https://images.mindcloud.co/apps/icons/images-10_1774543295136.png" alt="Scoro logo" width="28" height="28"> Scoro: Universal API

Manage contacts, projects, tasks, invoices, and professional services operations in Scoro.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scoro/latest
- **Category:** Productivity / Project Management
- **Actions:** 44
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scoro.com
- **Vendor API docs:** https://api.scoro.com/api/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (44)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Finance Accounts](actions/list-finance-accounts.md) | GET | Retrieves finance accounts from Scoro. |
| [View Finance Account](actions/view-finance-account.md) | GET | Retrieves finance account details from Scoro. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Delete Calendar Event](actions/delete-calendar-event.md) | DELETE | Deletes an existing calendar event from Scoro. |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves calendar events from Scoro. |
| [Update Calendar Event](actions/update-calendar-event.md) | PUT | Updates an existing calendar event in Scoro. |
| [View Calendar Event](actions/view-calendar-event.md) | GET | Retrieves calendar event details from Scoro. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Scoro. |
| [List Contact Filters](actions/list-contact-filters.md) | GET | Retrieves contact filters from Scoro. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Scoro. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Scoro. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Scoro. |
| [View Contact](actions/view-contact.md) | GET | Retrieves contact details from Scoro. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Scoro. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Scoro. |
| [Update File](actions/update-file.md) | PUT | Updates an existing file in Scoro. |
| [View File](actions/view-file.md) | GET | Retrieves file details from Scoro. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Scoro. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Scoro. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Scoro. |
| [View Project](actions/view-project.md) | GET | Retrieves project details from Scoro. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Delete Purchase Order](actions/delete-purchase-order.md) | DELETE | Deletes an existing purchase order from Scoro. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Scoro. |
| [Update Purchase Order](actions/update-purchase-order.md) | PUT | Updates an existing purchase order in Scoro. |
| [View Purchase Order](actions/view-purchase-order.md) | GET | Retrieves purchase order details from Scoro. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Permission Sets](actions/list-permission-sets.md) | GET | Retrieves permission sets from Scoro. |
| [View Permission Set](actions/view-permission-set.md) | GET | Retrieves permission set details from Scoro. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Scoro. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Scoro. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Scoro. |
| [View Task](actions/view-task.md) | GET | Retrieves task details from Scoro. |

### Tax Codes

| Action | Method | Description |
| --- | --- | --- |
| [List VAT Codes](actions/list-vat-codes.md) | GET | Retrieves VAT codes from Scoro. |
| [View VAT Code](actions/view-vat-code.md) | GET | Retrieves VAT code details from Scoro. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Client Profile](actions/delete-client-profile.md) | DELETE | Deletes an existing client profile from Scoro. |
| [List Client Profiles](actions/list-client-profiles.md) | GET | Retrieves client profiles from Scoro. |
| [List Event Resources](actions/list-event-resources.md) | GET | Retrieves event resources from Scoro. |
| [List Finance Objects](actions/list-finance-objects.md) | GET | Retrieves finance objects from Scoro. |
| [List Price List Variants](actions/list-price-list-variants.md) | GET | Retrieves price list variants from Scoro. |
| [List Price Lists](actions/list-price-lists.md) | GET | Retrieves price lists from Scoro. |
| [Update Client Profile](actions/update-client-profile.md) | PUT | Updates an existing client profile in Scoro. |
| [View Client Profile](actions/view-client-profile.md) | GET | Retrieves client profile details from Scoro. |
| [View Event Resource](actions/view-event-resource.md) | GET | Retrieves event resource details from Scoro. |
| [View Price List](actions/view-price-list.md) | GET | Retrieves price list details from Scoro. |
| [View Price List Variant](actions/view-price-list-variant.md) | GET | Retrieves price list variant details from Scoro. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [List Depots](actions/list-depots.md) | GET | Retrieves depots from Scoro. |

