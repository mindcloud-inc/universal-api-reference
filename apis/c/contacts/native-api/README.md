# Contacts+: Native API Reference

A consolidated summary of Contacts+'s API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://www.contactsplus.com/developers/contacts-api/
- **API base URL:** `https://api.contactsplus.com`

## Authentication

### OAuth2

OAuth 2.0 authorization for Contacts+ API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.contactsplus.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.contactsplus.com/v3/oauth.exchangeAuthCode.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account.read,contacts.read,contacts.write,tags.read,tags.write,teams.read,teams.contacts.read,teams.contacts.write,teams.tags.read,teams.tags.write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.contactsplus.com/v3/oauth.refreshToken.

[Official authentication documentation](https://www.contactsplus.com/developers/contacts-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `account`. The next-page cursor is read from `cursor`.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /api/v1/contacts.create` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/tags.create` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Delete Contact](actions/delete-contact.md) | `POST /api/v1/contacts.delete` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Delete Tag](actions/delete-tag.md) | `POST /api/v1/tags.delete` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Get Account](actions/get-account.md) | `POST /api/v1/account.get` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [List Contacts by ID](actions/list-contacts-by-id.md) | `POST /api/v1/contacts.get` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [List Tags by ID](actions/list-tags-by-id.md) | `POST /api/v1/tags.get` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [List Teams](actions/list-teams.md) | `POST /api/v1/teams.get` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Manage Contact Tags](actions/manage-contact-tags.md) | `POST /api/v1/contacts.manageTags` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Scroll Contacts](actions/scroll-contacts.md) | `POST /api/v1/contacts.scroll` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Scroll Tags](actions/scroll-tags.md) | `POST /api/v1/tags.scroll` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Search Contacts](actions/search-contacts.md) | `POST /api/v1/contacts.search` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Update Contact](actions/update-contact.md) | `POST /api/v1/contacts.update` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Update Tag](actions/update-tag.md) | `POST /api/v1/tags.update` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
| [Upload Contact Photo](actions/upload-contact-photo.md) | `POST /api/v1/contacts.uploadPhoto` | [docs](https://www.contactsplus.com/developers/contacts-api/) |
