# Scoro: Native API Reference

A consolidated summary of Scoro's API configuration and 44 documented operations, with links to official documentation.

- **Official docs:** https://api.scoro.com/api/v2
- **API base URL:** `{subdomain}`

## Authentication

### API Key

Use a Scoro API key plus your full Scoro API base URL and company account ID.

### Credentials

- **API Key:** `apiKey` · required
- **Company Account ID:** `companyAccountId` · required · The business entity identifier shown in Scoro Settings > External Connections > API.
- **Site Base URL:** `subdomain` · required · Enter the full Scoro API base URL, for example https://mindcloud.scoro.com/api/v2.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.scoro.com/api/v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the request body to set the page size (default 50; accepted range 1–100). Use `page` in the request body to choose the page; numbering starts at 1.

## Filtering

Send filters in the request body. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (44 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Calendar Event](actions/delete-calendar-event.md) | `POST calendar/delete/:id` | [docs](https://api.scoro.com/api/v2#calendarApiV2Docs) |
| [Delete Client Profile](actions/delete-client-profile.md) | `POST clientProfiles/delete/:id` | [docs](https://api.scoro.com/api/v2#clientProfilesApiV2Docs) |
| [Delete Contact](actions/delete-contact.md) | `POST contacts/delete/:id` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [Delete File](actions/delete-file.md) | `POST files/delete/:id` | [docs](https://api.scoro.com/api/v2#filesApiV2Docs) |
| [Delete Project](actions/delete-project.md) | `POST projects/delete/:id` | [docs](https://api.scoro.com/api/v2#projectsApiV2Docs) |
| [Delete Purchase Order](actions/delete-purchase-order.md) | `POST purchaseOrders/delete/:id` | [docs](https://api.scoro.com/api/v2#purchaseOrdersApiV2Docs) |
| [Delete Task](actions/delete-task.md) | `POST tasks/delete/:id` | [docs](https://api.scoro.com/api/v2#tasksApiV2Docs) |
| [List Calendar Events](actions/list-calendar-events.md) | `POST calendar/list` | [docs](https://api.scoro.com/api/v2#calendarApiV2Docs) |
| [List Client Profiles](actions/list-client-profiles.md) | `POST clientProfiles/list` | [docs](https://api.scoro.com/api/v2#clientProfilesApiV2Docs) |
| [List Contact Filters](actions/list-contact-filters.md) | `POST contacts/filters` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [List Contacts](actions/list-contacts.md) | `POST contacts/list` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [List Depots](actions/list-depots.md) | `POST depot/list` | [docs](https://api.scoro.com/api/v2#depotApiV2Docs) |
| [List Event Resources](actions/list-event-resources.md) | `POST eventsResources/list` | [docs](https://api.scoro.com/api/v2#eventsResourcesApiV2Docs) |
| [List Files](actions/list-files.md) | `POST files/list` | [docs](https://api.scoro.com/api/v2#filesApiV2Docs) |
| [List Finance Accounts](actions/list-finance-accounts.md) | `POST financeAccounts/list` | [docs](https://api.scoro.com/api/v2#financeAccountsApiV2Docs) |
| [List Finance Objects](actions/list-finance-objects.md) | `POST financeObjects/list` | [docs](https://api.scoro.com/api/v2#financeObjectsApiV2Docs) |
| [List Permission Sets](actions/list-permission-sets.md) | `POST userRoles/list` | [docs](https://api.scoro.com/api/v2#userRolesApiV2Docs) |
| [List Price List Variants](actions/list-price-list-variants.md) | `POST localPriceLists/list` | [docs](https://api.scoro.com/api/v2#localPriceListsApiV2Docs) |
| [List Price Lists](actions/list-price-lists.md) | `POST priceLists/list` | [docs](https://api.scoro.com/api/v2#priceListsApiV2Docs) |
| [List Projects](actions/list-projects.md) | `POST projects/list` | [docs](https://api.scoro.com/api/v2#projectsApiV2Docs) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `POST purchaseOrders/list` | [docs](https://api.scoro.com/api/v2#purchaseOrdersApiV2Docs) |
| [List Tasks](actions/list-tasks.md) | `POST tasks/list` | [docs](https://api.scoro.com/api/v2#tasksApiV2Docs) |
| [List VAT Codes](actions/list-vat-codes.md) | `POST vatCodes/list` | [docs](https://api.scoro.com/api/v2#vatCodesApiV2Docs) |
| [Search Contacts](actions/search-contacts.md) | `POST contacts` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [Update Calendar Event](actions/update-calendar-event.md) | `POST calendar/modify/:id` | [docs](https://api.scoro.com/api/v2#calendarApiV2Docs) |
| [Update Client Profile](actions/update-client-profile.md) | `POST clientProfiles/modify/:id` | [docs](https://api.scoro.com/api/v2#clientProfilesApiV2Docs) |
| [Update Contact](actions/update-contact.md) | `POST contacts/modify/:id` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [Update File](actions/update-file.md) | `POST files/modify/:id` | [docs](https://api.scoro.com/api/v2#filesApiV2Docs) |
| [Update Project](actions/update-project.md) | `POST projects/modify/:id` | [docs](https://api.scoro.com/api/v2#projectsApiV2Docs) |
| [Update Purchase Order](actions/update-purchase-order.md) | `POST purchaseOrders/modify/:id` | [docs](https://api.scoro.com/api/v2#purchaseOrdersApiV2Docs) |
| [Update Task](actions/update-task.md) | `POST tasks/modify/:id` | [docs](https://api.scoro.com/api/v2#tasksApiV2Docs) |
| [View Calendar Event](actions/view-calendar-event.md) | `POST calendar/view/:id` | [docs](https://api.scoro.com/api/v2#calendarApiV2Docs) |
| [View Client Profile](actions/view-client-profile.md) | `POST clientProfiles/view/:id` | [docs](https://api.scoro.com/api/v2#clientProfilesApiV2Docs) |
| [View Contact](actions/view-contact.md) | `POST contacts/view/:id` | [docs](https://api.scoro.com/api/v2#contactsApiV2Docs) |
| [View Event Resource](actions/view-event-resource.md) | `POST eventsResources/view/:id` | [docs](https://api.scoro.com/api/v2#eventsResourcesApiV2Docs) |
| [View File](actions/view-file.md) | `POST files/view/:id` | [docs](https://api.scoro.com/api/v2#filesApiV2Docs) |
| [View Finance Account](actions/view-finance-account.md) | `POST financeAccounts/view/:id` | [docs](https://api.scoro.com/api/v2#financeAccountsApiV2Docs) |
| [View Permission Set](actions/view-permission-set.md) | `POST userRoles/view/:id` | [docs](https://api.scoro.com/api/v2#userRolesApiV2Docs) |
| [View Price List](actions/view-price-list.md) | `POST priceLists/view/:id` | [docs](https://api.scoro.com/api/v2#priceListsApiV2Docs) |
| [View Price List Variant](actions/view-price-list-variant.md) | `POST localPriceLists/view/:id` | [docs](https://api.scoro.com/api/v2#localPriceListsApiV2Docs) |
| [View Project](actions/view-project.md) | `POST projects/view/:id` | [docs](https://api.scoro.com/api/v2#projectsApiV2Docs) |
| [View Purchase Order](actions/view-purchase-order.md) | `POST purchaseOrders/view/:id` | [docs](https://api.scoro.com/api/v2#purchaseOrdersApiV2Docs) |
| [View Task](actions/view-task.md) | `POST tasks/view/:id` | [docs](https://api.scoro.com/api/v2#tasksApiV2Docs) |
| [View VAT Code](actions/view-vat-code.md) | `POST vatCodes/view/:id` | [docs](https://api.scoro.com/api/v2#vatCodesApiV2Docs) |
