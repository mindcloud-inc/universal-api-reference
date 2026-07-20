# Keap: Native API Reference

A consolidated summary of Keap's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.keap.com/docs/restv2/
- **OpenAPI specification:** https://api.infusionsoft.com/info-service/crm/docs/rest/V2
- **API base URL:** `https://api.infusionsoft.com/crm/rest/v2`

## Authentication

### OAuth2

Connect to Keap using OAuth2 authorization

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.infusionsoft.com/app/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.infusionsoft.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.infusionsoft.com/token.

[Official authentication documentation](https://developer.infusionsoft.com/getting-started-oauth-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `page_size` in the query string to set the page size (default 25; accepted range 0–1000). Use `page_token` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `order_by` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Tag To Contacts](actions/apply-tag-to-contacts.md) | `POST /tags/{tag_id}/contacts:applyTags` | [docs](https://developer.keap.com/docs/restv2/#tag/Tag/operation/applyTags) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://developer.keap.com/docs/restv2/#tag/Company/operation/createCompany) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.keap.com/docs/restv2/#tag/Contact/operation/createContact) |
| [Create Note](actions/create-note.md) | `POST /contacts/{contact_id}/notes` | [docs](https://developer.keap.com/docs/restv2/#tag/Note/operation/createNote) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /opportunities` | [docs](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/createOpportunity) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developer.keap.com/docs/restv2/#tag/Tag/operation/createTag) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developer.keap.com/docs/restv2/#tag/Task/operation/createTask) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{contact_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Contact/operation/deleteContact) |
| [Get Company](actions/get-company.md) | `GET /companies/:company_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Company/operation/getCompany) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Contact/operation/getContact) |
| [Get File](actions/get-file.md) | `GET /files/:file_id` | [docs](https://developer.keap.com/docs/restv2/#tag/File/operation/getFile) |
| [Get Note](actions/get-note.md) | `GET /contacts/:contact_id/notes/:note_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Note/operation/getNote) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /opportunities/:opportunity_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/getOpportunity) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tag_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Tag/operation/getTag) |
| [Get Task](actions/get-task.md) | `GET /tasks/:task_id` | [docs](https://developer.keap.com/docs/restv2/#tag/Task/operation/getTask) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developer.keap.com/docs/restv2/#tag/Company/operation/listCompanies) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.keap.com/docs/restv2/#tag/Contact/operation/listContacts) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://developer.keap.com/docs/restv2/#tag/Email/operation/listEmails) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://developer.keap.com/docs/restv2/#tag/File/operation/listFiles) |
| [List Notes](actions/list-notes.md) | `GET /contacts/:contact_id/notes` | [docs](https://developer.keap.com/docs/restv2/#tag/Note/operation/listNotes) |
| [List Opportunities](actions/list-opportunities.md) | `GET /opportunities` | [docs](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/listOpportunities) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.keap.com/docs/restv2/#tag/Tag/operation/listTags) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developer.keap.com/docs/restv2/#tag/Task/operation/listTasks) |
| [Remove Tags From Contacts](actions/remove-tags-from-contacts.md) | `POST /tags/{tag_id}/contacts:removeTags` | [docs](https://developer.keap.com/docs/restv2/#tag/Tag/operation/removeTags) |
| [Send Email](actions/send-email.md) | `POST /emails:send` | [docs](https://developer.keap.com/docs/restv2/#tag/Email/operation/sendEmail) |
| [Update Company](actions/update-company.md) | `PATCH /companies/{company_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Company/operation/updateCompany) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{contact_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Contact/operation/updateContact) |
| [Update Note](actions/update-note.md) | `PATCH /contacts/{contact_id}/notes/{note_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Note/operation/updateNote) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /opportunities/{opportunity_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Opportunity/operation/updateOpportunity) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/{task_id}` | [docs](https://developer.keap.com/docs/restv2/#tag/Task/operation/updateTask) |
