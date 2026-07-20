# Salesmate: Native API Reference

A consolidated summary of Salesmate's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.salesmate.io/
- **API base URL:** `https://apis.salesmate.io`

## Authentication

### API Key

Use a Salesmate session token and your full Salesmate account domain.

### Credentials

- **API Key:** `apiKey` · required
- **Link Domain:** `linkDomain` · required · Full Salesmate account domain, for example demo.salesmate.io.

Send these headers with each API request:

```http
x-linkname: <linkDomain>
accessToken: <apiKey>
```

[Official authentication documentation](https://apidocs.salesmate.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Activity](actions/add-activity.md) | `POST /activity/v4` | [docs](https://apidocs.salesmate.io/) |
| [Add Company](actions/add-company.md) | `POST /company/v4` | [docs](https://apidocs.salesmate.io/) |
| [Add Company Note](actions/add-company-note.md) | `POST /company/v4/modules/5/object/:companyId/notes` | [docs](https://apidocs.salesmate.io/) |
| [Add Contact](actions/add-contact.md) | `POST /contact/v4` | [docs](https://apidocs.salesmate.io/) |
| [Add Contact Note](actions/add-contact-note.md) | `POST /contact/v4/modules/1/object/:contactId/notes` | [docs](https://apidocs.salesmate.io/) |
| [Add Deal](actions/add-deal.md) | `POST /deal/v4` | [docs](https://apidocs.salesmate.io/) |
| [Add Deal Note](actions/add-deal-note.md) | `POST /deal/v4/modules/4/object/:dealId/notes` | [docs](https://apidocs.salesmate.io/) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /activity/v4/:activityId` | [docs](https://apidocs.salesmate.io/) |
| [Delete Company](actions/delete-company.md) | `DELETE /company/v4/:companyId` | [docs](https://apidocs.salesmate.io/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/v4/:contactId` | [docs](https://apidocs.salesmate.io/) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /deal/v4/:dealId` | [docs](https://apidocs.salesmate.io/) |
| [Get Active Users](actions/get-active-users.md) | `GET /core/v4/users` | [docs](https://apidocs.salesmate.io/) |
| [Get Activity](actions/get-activity.md) | `GET /activity/v4/:activityId` | [docs](https://apidocs.salesmate.io/) |
| [Get Company](actions/get-company.md) | `GET /company/v4/:companyId` | [docs](https://apidocs.salesmate.io/) |
| [Get Contact](actions/get-contact.md) | `GET /contact/v4/:contactId` | [docs](https://apidocs.salesmate.io/) |
| [Get Deal](actions/get-deal.md) | `GET /deal/v4/:dealId` | [docs](https://apidocs.salesmate.io/) |
| [Search Activities](actions/search-activities.md) | `POST /activity/v4/search` | [docs](https://apidocs.salesmate.io/) |
| [Search Companies](actions/search-companies.md) | `POST /company/v4/search` | [docs](https://apidocs.salesmate.io/) |
| [Search Contacts](actions/search-contacts.md) | `POST /contact/v4/search` | [docs](https://apidocs.salesmate.io/) |
| [Search Deals](actions/search-deals.md) | `POST /deal/v4/search` | [docs](https://apidocs.salesmate.io/) |
| [Update Activity](actions/update-activity.md) | `PUT /activity/v4/:activityId` | [docs](https://apidocs.salesmate.io/) |
| [Update Company](actions/update-company.md) | `PUT /company/v4/:companyId` | [docs](https://apidocs.salesmate.io/) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/v4/:contactId` | [docs](https://apidocs.salesmate.io/) |
| [Update Deal](actions/update-deal.md) | `PUT /deal/v4/:dealId` | [docs](https://apidocs.salesmate.io/) |
