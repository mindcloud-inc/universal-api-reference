# Benchmark Email: Native API Reference

A consolidated summary of Benchmark Email's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.benchmarkemail.com/
- **API base URL:** `https://clientapi.benchmarkemail.com`

## Authentication

### API Key

Use a Benchmark Admin API token in the AuthToken header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
AuthToken: <apiKey>
```

[Official authentication documentation](https://developer.benchmarkemail.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `PageSize` in the query string to set the page size. Use `PageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `OrderBy` in the query string. Set the direction separately with `SortOrder`. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /Contact/:listId/ContactDetails` | [docs](https://developer.benchmarkemail.com) |
| [Create Contact List](actions/create-contact-list.md) | `POST /Contact/` | [docs](https://developer.benchmarkemail.com) |
| [Create Contact Segment](actions/create-contact-segment.md) | `POST /Contact/:listId/Segments` | [docs](https://developer.benchmarkemail.com) |
| [Create Email](actions/create-email.md) | `POST /Emails/` | [docs](https://developer.benchmarkemail.com) |
| [Get Automation](actions/get-automation.md) | `GET /Automation/:automationId` | [docs](https://developer.benchmarkemail.com) |
| [Get Automation Report](actions/get-automation-report.md) | `GET /Automation/:automationId/Report` | [docs](https://developer.benchmarkemail.com) |
| [Get Client Details](actions/get-client-details.md) | `GET /Client/` | [docs](https://developer.benchmarkemail.com) |
| [Get Contact](actions/get-contact.md) | `GET /Contact/:listId/ContactDetails/:id` | [docs](https://developer.benchmarkemail.com) |
| [Get Contact List](actions/get-contact-list.md) | `GET /Contact/:listId` | [docs](https://developer.benchmarkemail.com) |
| [Get Contact Segment](actions/get-contact-segment.md) | `GET /Contact/Segments/:segmentId` | [docs](https://developer.benchmarkemail.com) |
| [Get Email](actions/get-email.md) | `GET /Emails/:id` | [docs](https://developer.benchmarkemail.com) |
| [Get Email Preview](actions/get-email-preview.md) | `GET /Emails/:id/Preview` | [docs](https://developer.benchmarkemail.com) |
| [Get Plan](actions/get-plan.md) | `GET /Client/Plan` | [docs](https://developer.benchmarkemail.com) |
| [Get Profile Details](actions/get-profile-details.md) | `GET /Client/ProfileDetails` | [docs](https://developer.benchmarkemail.com/#da6e98f3-94b7-b0e0-b07b-cd6ae5541e45) |
| [List Automations](actions/list-automations.md) | `GET /Automation/` | [docs](https://developer.benchmarkemail.com) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /Contact/` | [docs](https://developer.benchmarkemail.com) |
| [List Contact Segments](actions/list-contact-segments.md) | `GET /Contact/Segments` | [docs](https://developer.benchmarkemail.com) |
| [List Contacts](actions/list-contacts.md) | `GET /Contact/:listId/ContactDetails` | [docs](https://developer.benchmarkemail.com) |
| [List Email Reports](actions/list-email-reports.md) | `GET /Emails/Report` | [docs](https://developer.benchmarkemail.com) |
| [Schedule Email](actions/schedule-email.md) | `POST /Emails/:id/Schedule` | [docs](https://developer.benchmarkemail.com) |
| [Search Contacts](actions/search-contacts.md) | `GET /Contact/ContactDetails` | [docs](https://developer.benchmarkemail.com) |
| [Update Contact](actions/update-contact.md) | `PATCH /Contact/:listId/ContactDetails/:contactId` | [docs](https://developer.benchmarkemail.com) |
| [Update Contact List](actions/update-contact-list.md) | `PATCH /Contact/:listId` | [docs](https://developer.benchmarkemail.com) |
| [Update Email](actions/update-email.md) | `PATCH /Emails/:id` | [docs](https://developer.benchmarkemail.com) |
