# Dotdigital: Native API Reference

A consolidated summary of Dotdigital's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developer.dotdigital.com/reference
- **API base URL:** `https://r2-api.dotmailer.com`

## Authentication

### Basic Auth

Connect with your dotdigital API username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **API Endpoint:** `apiEndpoint` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.dotdigital.com/docs/setting-up-an-api-user)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `select` in the query string to set the page size (default 1000; accepted range 1–1000). Use `skip` in the query string as the record offset.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /v2/campaigns` | [docs](https://developer.dotdigital.com/reference/create-campaign) |
| [Create Template](actions/create-template.md) | `POST /v2/templates` | [docs](https://developer.dotdigital.com/reference/create-template) |
| [Get Account Information](actions/get-account-information.md) | `GET /v2/account-info` | [docs](https://developer.dotdigital.com/reference/get-account-information) |
| [Get All Campaigns With Filters](actions/get-all-campaigns-with-filters.md) | `GET /v2/campaigns/filtered` | [docs](https://developer.dotdigital.com/reference/get-all-campaigns-with-filters) |
| [Get All Custom Identifiers](actions/get-all-custom-identifiers.md) | `GET /configuration/v3/customIdentifiers` | [docs](https://developer.dotdigital.com/reference/getcustomidentifiers) |
| [Get Campaign](actions/get-campaign.md) | `GET /v2/campaigns/:id` | [docs](https://developer.dotdigital.com/reference/get-campaign) |
| [Get Campaign Send Status](actions/get-campaign-send-status.md) | `GET /v2/campaigns/send/:id` | [docs](https://developer.dotdigital.com/reference/get-campaign-send-status) |
| [Get Campaign Summary](actions/get-campaign-summary.md) | `GET /v2/campaigns/:id/summary` | [docs](https://developer.dotdigital.com/reference/get-campaign-summary) |
| [Get Campaign With Details](actions/get-campaign-with-details.md) | `GET /v2/campaigns/:id/with-details` | [docs](https://developer.dotdigital.com/reference/get-campaign-with-details) |
| [Get Contact Data Fields](actions/get-contact-data-fields.md) | `GET /v2/data-fields` | [docs](https://developer.dotdigital.com/reference/get-contact-data-fields) |
| [Get Contacts Based on Your Criteria](actions/get-contacts-based-on-your-criteria.md) | `GET /contacts/v3` | [docs](https://developer.dotdigital.com/reference/getcontacts-1) |
| [Get Form by ID](actions/get-form-by-id.md) | `GET /v2/surveys/:id` | [docs](https://developer.dotdigital.com/reference/get-form-by-id) |
| [Get Forms](actions/get-forms.md) | `GET /v2/surveys` | [docs](https://developer.dotdigital.com/reference/get-forms) |
| [Get List](actions/get-list.md) | `GET /v2/address-books/:id` | [docs](https://developer.dotdigital.com/reference/get-address-book) |
| [Get Lists](actions/get-lists.md) | `GET /v2/address-books` | [docs](https://developer.dotdigital.com/reference/get-address-books) |
| [Get Preferences](actions/get-preferences.md) | `GET /v2/preferences` | [docs](https://developer.dotdigital.com/reference/get-preferences) |
| [Get Preferences for Contact](actions/get-preferences-for-contact.md) | `GET /v2/contacts/:contactIdentifier/preferences` | [docs](https://developer.dotdigital.com/reference/get-preferences-for-contact) |
| [Get Private Lists](actions/get-private-lists.md) | `GET /v2/address-books/private` | [docs](https://developer.dotdigital.com/reference/get-private-address-books) |
| [Get Program by ID](actions/get-program-by-id.md) | `GET /v2/programs/:id` | [docs](https://developer.dotdigital.com/reference/get-program-by-id) |
| [Get Programs](actions/get-programs.md) | `GET /v2/programs` | [docs](https://developer.dotdigital.com/reference/get-programs) |
| [Get Public Lists](actions/get-public-lists.md) | `GET /v2/address-books/public` | [docs](https://developer.dotdigital.com/reference/get-public-address-books) |
| [Get Segments](actions/get-segments.md) | `GET /v2/segments` | [docs](https://developer.dotdigital.com/reference/get-segments) |
| [Get Subscriptions for Contact](actions/get-subscriptions-for-contact.md) | `GET /v2/contacts/:email/subscriptions` | [docs](https://developer.dotdigital.com/reference/get-subscriptions-for-contact) |
| [Get Template by ID](actions/get-template-by-id.md) | `GET /v2/templates/:id` | [docs](https://developer.dotdigital.com/reference/get-template-by-id) |
| [Get Templates](actions/get-templates.md) | `GET /v2/templates` | [docs](https://developer.dotdigital.com/reference/get-templates) |
| [Retrieve a Contact by an Identifier](actions/retrieve-a-contact-by-an-identifier.md) | `GET /contacts/v3/:identifier/:value` | [docs](https://developer.dotdigital.com/reference/getcontact) |
