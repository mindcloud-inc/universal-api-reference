# Moco: Native API Reference

A consolidated summary of Moco's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://everii-group.github.io/mocoapp-api-docs/
- **API base URL:** `https://{domain}.mocoapp.com/api/v1`

## Authentication

### API Key

Authenticate MOCO API requests with a personal or account API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Domain:** `domain` · required · MOCO account subdomain used in https://{domain}.mocoapp.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://everii-group.github.io/mocoapp-api-docs/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activities` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#post-activities) |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#post-comments) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/companies.html#post-companies) |
| [Create Contact](actions/create-contact.md) | `POST /contacts/people` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/contacts.html#post-contactspeople) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#post-deals) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#post-invoices) |
| [Create Offer](actions/create-offer.md) | `POST /offers` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#post-offers) |
| [Create Planning Entry](actions/create-planning-entry.md) | `POST /planning_entries` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#post-planning_entries) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#post-projects) |
| [Create Purchase](actions/create-purchase.md) | `POST /purchases` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#post-purchases) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/schedules.html#post-schedules) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/users.html#post-users) |
| [Get Activity](actions/get-activity.md) | `GET /activities/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#get-activitiesid) |
| [Get Comment](actions/get-comment.md) | `GET /comments/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#get-commentsid) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/companies.html#get-companiesid) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/people/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/contacts.html#get-contactspeopleid) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#get-dealsid) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#get-invoicesid) |
| [Get Offer](actions/get-offer.md) | `GET /offers/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#get-offersid) |
| [Get Profile](actions/get-profile.md) | `GET /profile` | [docs](https://everii-group.github.io/mocoapp-api-docs/profile/get_profile.html) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#get-projectsid) |
| [Get Purchase](actions/get-purchase.md) | `GET /purchases/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#get-purchasesid) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/users.html#get-usersid) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#get-activities) |
| [List Assigned Projects](actions/list-assigned-projects.md) | `GET /projects/assigned` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#get-projectsassigned) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#get-comments) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/companies.html#get-companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/people` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/contacts.html#get-contactspeople) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#get-deals) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#get-invoices) |
| [List Offers](actions/list-offers.md) | `GET /offers` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#get-offers) |
| [List Planning Entries](actions/list-planning-entries.md) | `GET /planning_entries` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#get-planning_entries) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#get-projects) |
| [List Purchases](actions/list-purchases.md) | `GET /purchases` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#get-purchases) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/schedules.html#get-schedules) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/users.html#get-users) |
| [Update Activity](actions/update-activity.md) | `PUT /activities/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/activities.html#put-activitiesid) |
| [Update Comment](actions/update-comment.md) | `PUT /comments/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#put-commentsid) |
| [Update Company](actions/update-company.md) | `PUT /companies/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/companies.html#put-companiesid) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/people/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/contacts.html#put-contactspeopleid) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/deals.html#put-dealsid) |
| [Update Invoice Status](actions/update-invoice-status.md) | `PUT /invoices/:id/update_status` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/invoices.html#put-invoicesidupdate_status) |
| [Update Offer Status](actions/update-offer-status.md) | `PUT /offers/:id/update_status` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/offers.html#put-offersidupdate_status) |
| [Update Planning Entry](actions/update-planning-entry.md) | `PUT /planning_entries/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/planning_entries.html#put-planning_entriesid) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#put-projectsid) |
| [Update Purchase](actions/update-purchase.md) | `PUT /purchases/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/purchases.html#put-purchasesid) |
| [Update Schedule](actions/update-schedule.md) | `PUT /schedules/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/schedules.html#put-schedulesid) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://everii-group.github.io/mocoapp-api-docs/sections/users.html#put-usersid) |
