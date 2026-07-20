# OnePageCRM: Native API Reference

A consolidated summary of OnePageCRM's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developer.onepagecrm.com/api/
- **OpenAPI specification:** https://raw.githubusercontent.com/OnePageCRM/swagger/master/swagger.yaml
- **API base URL:** `https://app.onepagecrm.com/api/v3`

## Authentication

### API Key

Connect with your OnePageCRM API key and user ID.

### Credentials

- **API Key:** `apiKey` · required
- **User ID:** `userId` · required · Your OnePageCRM user_id, used with the API key to authenticate requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.onepagecrm.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `max_page`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Contact Owner](actions/change-contact-owner.md) | `PUT /contacts/:contact_id/change_owner/:owner_id` | [docs](https://developer.onepagecrm.com/api/#/Contacts/put_contacts_contact_id_change_owner_owner_id) |
| [Change Contact Status](actions/change-contact-status.md) | `PUT /contacts/:contact_id/change_status/:status_id` | [docs](https://developer.onepagecrm.com/api/#/Contacts/put_contacts_contact_id_change_status_status_id) |
| [Create Action](actions/create-action.md) | `POST /actions` | [docs](https://developer.onepagecrm.com/api/#/Actions/post_actions) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.onepagecrm.com/api/#/Contacts/post_contacts) |
| [Create Deal](actions/create-deal.md) | `POST /deals` | [docs](https://developer.onepagecrm.com/api/#/Deals/post_deals) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://developer.onepagecrm.com/api/#/Notes/post_notes) |
| [Get Action](actions/get-action.md) | `GET /actions/:action_id` | [docs](https://developer.onepagecrm.com/api/#/Actions/get_actions__action_id_) |
| [Get Company](actions/get-company.md) | `GET /companies/:company_id` | [docs](https://developer.onepagecrm.com/api/#/Companies/get_companies__company_id_) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://developer.onepagecrm.com/api/#/Contacts/get_contacts_contact_id) |
| [Get Deal](actions/get-deal.md) | `GET /deals/:deal_id` | [docs](https://developer.onepagecrm.com/api/#/Deals/get_deals__deal_id_) |
| [List Action Stream Contacts](actions/list-action-stream-contacts.md) | `GET /action_stream` | [docs](https://developer.onepagecrm.com/api/#/Action_Stream/get_action_stream) |
| [List Actions](actions/list-actions.md) | `GET /actions` | [docs](https://developer.onepagecrm.com/api/#/Actions/get_actions) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developer.onepagecrm.com/api/#/Companies/get_companies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.onepagecrm.com/api/#/Contacts/get_contacts) |
| [List Deals](actions/list-deals.md) | `GET /deals` | [docs](https://developer.onepagecrm.com/api/#/Deals/get_deals) |
| [List Lead Sources](actions/list-lead-sources.md) | `GET /lead_sources` | [docs](https://developer.onepagecrm.com/api/#/Lead%20Sources/get_lead_sources) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://developer.onepagecrm.com/api/#/Notes/get_notes) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines` | [docs](https://developer.onepagecrm.com/api/#/Pipelines/get_pipelines) |
| [List Statuses](actions/list-statuses.md) | `GET /statuses` | [docs](https://developer.onepagecrm.com/api/#/Statuses/get_statuses) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.onepagecrm.com/api/#/Users/get_users) |
| [Mark Action as Done](actions/mark-action-as-done.md) | `PUT /actions/:action_id/mark_as_done` | [docs](https://developer.onepagecrm.com/api/#/Actions/put_actions__action_id__mark_as_done) |
| [Update Action](actions/update-action.md) | `PUT /actions/:action_id` | [docs](https://developer.onepagecrm.com/api/#/Actions/put_actions__action_id_) |
| [Update Company](actions/update-company.md) | `PUT /companies/:company_id` | [docs](https://developer.onepagecrm.com/api/#/Companies/put_companies__company_id_) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://developer.onepagecrm.com/api/#/Contacts/put_contacts_contact_id) |
| [Update Deal](actions/update-deal.md) | `PUT /deals/:deal_id` | [docs](https://developer.onepagecrm.com/api/#/Deals/put_deals__deal_id_) |
