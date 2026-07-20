# Google Contacts: Native API Reference

A consolidated summary of Google Contacts's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/people/api/rest
- **API base URL:** `https://people.googleapis.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/contacts openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `connections`. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | `POST /v1/people\:batchCreateContacts` | [docs](https://developers.google.com/people/api/rest/v1/people/batchCreateContacts) |
| [Batch Delete Contacts](actions/batch-delete-contacts.md) | `POST /v1/people\:batchDeleteContacts` | [docs](https://developers.google.com/people/api/rest/v1/people/batchDeleteContacts) |
| [Batch Get Contact Groups](actions/batch-get-contact-groups.md) | `GET /v1/contactGroups\:batchGet` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/batchGet) |
| [Batch Get People](actions/batch-get-people.md) | `GET /v1/people\:batchGet` | [docs](https://developers.google.com/people/api/rest/v1/people/getBatchGet) |
| [Batch Update Contacts](actions/batch-update-contacts.md) | `POST /v1/people\:batchUpdateContacts` | [docs](https://developers.google.com/people/api/rest/v1/people/batchUpdateContacts) |
| [Copy Other Contact To My Contacts Group](actions/copy-other-contact-to-my-contacts-group.md) | `POST /v1/otherContacts/:resourceName:copyAction` | [docs](https://developers.google.com/people/api/rest/v1/otherContacts/copyOtherContactToMyContactsGroup) |
| [Create Contact](actions/create-contact.md) | `POST /v1/people\:createContact` | [docs](https://developers.google.com/people/api/rest/v1/people/createContact) |
| [Create Contact Group](actions/create-contact-group.md) | `POST /v1/contactGroups` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/create) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/people/:resourceName:contactAction` | [docs](https://developers.google.com/people/api/rest/v1/people/deleteContact) |
| [Delete Contact Group](actions/delete-contact-group.md) | `DELETE /v1/contactGroups/:resourceName` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/delete) |
| [Delete Contact Photo](actions/delete-contact-photo.md) | `DELETE /v1/people/:resourceName:photoAction` | [docs](https://developers.google.com/people/api/rest/v1/people/deleteContactPhoto) |
| [Get Contact Group](actions/get-contact-group.md) | `GET /v1/contactGroups/:resourceName` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/get) |
| [Get Person](actions/get-person.md) | `GET /v1/people/:resourceName` | [docs](https://developers.google.com/people/api/rest/v1/people/get) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /v1/contactGroups` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/list) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/people/me/connections` | [docs](https://developers.google.com/people/api/rest/v1/people.connections/list) |
| [List Directory People](actions/list-directory-people.md) | `GET /v1/people\:listDirectoryPeople` | [docs](https://developers.google.com/people/api/rest/v1/people/listDirectoryPeople) |
| [List Other Contacts](actions/list-other-contacts.md) | `GET /v1/otherContacts` | [docs](https://developers.google.com/people/api/rest/v1/otherContacts/list) |
| [Modify Contact Group Members](actions/modify-contact-group-members.md) | `POST /v1/contactGroups/:resourceName/members\:modify` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups.members/modify) |
| [Search Contacts](actions/search-contacts.md) | `GET /v1/people\:searchContacts` | [docs](https://developers.google.com/people/api/rest/v1/people/searchContacts) |
| [Search Directory People](actions/search-directory-people.md) | `GET /v1/people\:searchDirectoryPeople` | [docs](https://developers.google.com/people/api/rest/v1/people/searchDirectoryPeople) |
| [Search Other Contacts](actions/search-other-contacts.md) | `GET /v1/otherContacts\:search` | [docs](https://developers.google.com/people/api/rest/v1/otherContacts/search) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/people/:resourceName:contactAction` | [docs](https://developers.google.com/people/api/rest/v1/people/updateContact) |
| [Update Contact Group](actions/update-contact-group.md) | `PUT /v1/contactGroups/:resourceName` | [docs](https://developers.google.com/people/api/rest/v1/contactGroups/update) |
| [Update Contact Photo](actions/update-contact-photo.md) | `PATCH /v1/people/:resourceName:photoAction` | [docs](https://developers.google.com/people/api/rest/v1/people/updateContactPhoto) |
