# RightSignature: Native API Reference

A consolidated summary of RightSignature's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://api.rightsignature.com/documentation/getting_started
- **API base URL:** `https://api.rightsignature.com/public/v2`

## Authentication

### OAuth 2.0

Connect a RightSignature account with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://secure.sharefile.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.authorizeRequest.subdomain}}.{{credentials.authorizeRequest.apicp}}/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.authorizeRequest.subdomain}}.{{credentials.authorizeRequest.apicp}}/oauth/token.

[Official authentication documentation](https://api.sharefile.com/gettingstarted/oauth2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Or Update Reusable Template Tags](actions/add-or-update-reusable-template-tags.md) | `PATCH /reusable_templates/:reusable_template_id/tags` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/update.en.html) |
| [Create Sending Request](actions/create-sending-request.md) | `POST /sending_requests` | [docs](https://api.rightsignature.com/documentation/resources/v2/sending_requests/create.en.html) |
| [Delete Reusable Template](actions/delete-reusable-template.md) | `DELETE /reusable_templates/:id` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/destroy.en.html) |
| [Delete Reusable Template Tag](actions/delete-reusable-template-tag.md) | `DELETE /reusable_templates/:reusable_template_id/tags` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/destroy.en.html) |
| [Embed Document From Reusable Template](actions/embed-document-from-reusable-template.md) | `POST /reusable_templates/:id/embed_document` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/embed_document.en.html) |
| [Get Archived Document By Original GUID](actions/get-archived-document-by-original-guid.md) | `GET /archived_documents_by_original_guid/:original_guid` | [docs](https://api.rightsignature.com/documentation/resources/v2/archived_documents/find_by_original_guid.en.html) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/show.en.html) |
| [Get Me](actions/get-me.md) | `GET /me` | [docs](https://api.rightsignature.com/documentation/resources/v2/users/me.en.html) |
| [Get Reusable Template](actions/get-reusable-template.md) | `GET /reusable_templates/:id` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/show.en.html) |
| [Get Sending Request](actions/get-sending-request.md) | `GET /sending_requests/:id` | [docs](https://api.rightsignature.com/documentation/resources/v2/sending_requests/show.en.html) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/index.en.html) |
| [List Reusable Template Tags](actions/list-reusable-template-tags.md) | `GET /reusable_templates/:reusable_template_id/tags` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/show.en.html) |
| [List Reusable Templates](actions/list-reusable-templates.md) | `GET /reusable_templates` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/index.en.html) |
| [Mark Sending Request Uploaded](actions/mark-sending-request-uploaded.md) | `POST /sending_requests/:id/uploaded` | [docs](https://api.rightsignature.com/documentation/resources/v2/sending_requests/uploaded.en.html) |
| [Merge And Send Document](actions/merge-and-send-document.md) | `POST /reusable_templates/:id/merge_and_send_document` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/merge_and_send_document.en.html) |
| [Prepare Document From Reusable Template](actions/prepare-document-from-reusable-template.md) | `POST /reusable_templates/:id/prepare_document` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/prepare_document.en.html) |
| [Replace Reusable Template Tags](actions/replace-reusable-template-tags.md) | `POST /reusable_templates/:reusable_template_id/tags` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/create.en.html) |
| [Request OAuth Access Token](actions/request-oauth-access-token.md) | `POST https://api.rightsignature.com/oauth/token` | [docs](https://api.rightsignature.com/documentation/resources/v2/oauth_tokens/create.en.html) |
| [Request OAuth Authorization Code](actions/request-oauth-authorization-code.md) | `GET https://api.rightsignature.com/oauth/authorize` | [docs](https://api.rightsignature.com/documentation/resources/v2/oauth_authorizations/default_url_options.en.html) |
| [Revoke OAuth Access Token](actions/revoke-oauth-access-token.md) | `POST https://api.rightsignature.com/oauth/revoke` | [docs](https://api.rightsignature.com/documentation/resources/v2/oauth_tokens/revoke.en.html) |
| [Send Document From Reusable Template](actions/send-document-from-reusable-template.md) | `POST /reusable_templates/:id/send_document` | [docs](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/send_document.en.html) |
| [Send Signer Reminder](actions/send-signer-reminder.md) | `POST /signers/:id/reminders` | [docs](https://api.rightsignature.com/documentation/resources/v2/signers/reminders.en.html) |
| [Share Document](actions/share-document.md) | `POST /documents/:id/share` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/share.en.html) |
| [Update Document PIN](actions/update-document-pin.md) | `PUT /documents/:id/update_pin` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/update_pin.en.html) |
| [Update Document Tags](actions/update-document-tags.md) | `POST /documents/:id/update_tags` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/update_tags.en.html) |
| [Void Document](actions/void-document.md) | `POST /documents/:id/void` | [docs](https://api.rightsignature.com/documentation/resources/v2/documents/void.en.html) |
