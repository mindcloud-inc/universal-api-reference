# SurveySparrow: Native API Reference

A consolidated summary of SurveySparrow's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://developers.surveysparrow.com/rest-apis/
- **API base URL:** `https://api.surveysparrow.com/v3`

## Authentication

### OAuth2

OAuth 2.0 authorization code flow for SurveySparrow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.surveysparrow.com/o/oauth/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.surveysparrow.com/o/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `view_survey view_questions`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.surveysparrow.com/o/oauth/token.

[Official authentication documentation](https://developers.surveysparrow.com/rest-apis/OAuth/)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Audit Log Event](actions/create-audit-log-event.md) | `POST /audit_logs/events` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-audit-logs-events/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-contacts/) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contact_lists` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-contact-lists/) |
| [Create Contact Property](actions/create-contact-property.md) | `POST /contact_properties` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-contact-properties/) |
| [Create Language](actions/create-language.md) | `POST /language` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-language/) |
| [Create Survey Folder](actions/create-survey-folder.md) | `POST /survey_folders` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-survey-folders/) |
| [Create Survey Variables](actions/create-survey-variables.md) | `POST /variables/batch` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-variables-batch/) |
| [Create Variable](actions/create-variable.md) | `POST /variables` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-variables/) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.surveysparrow.com/rest-apis/post-v-3-webhooks/) |
| [Delete Audit Log Event](actions/delete-audit-log-event.md) | `DELETE /audit_logs/events/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-audit-logs-events-id/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-contacts-id/) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contact_lists/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-contact-lists-id/) |
| [Delete Contact Property](actions/delete-contact-property.md) | `DELETE /contact_properties/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-contact-properties-id/) |
| [Delete Survey Folder](actions/delete-survey-folder.md) | `DELETE /survey_folders/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-survey-folders-id/) |
| [Delete Variable](actions/delete-variable.md) | `DELETE /variables/{{variableId}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-variables-variable-id/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/delete-v-3-webhooks-id/) |
| [Export Translation](actions/export-translation.md) | `GET /translation/export` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-translation-export/) |
| [Get Audit Log](actions/get-audit-log.md) | `GET /audit_logs/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-audit-logs-id/) |
| [Get Channel](actions/get-channel.md) | `GET /channels/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-channels-id/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-contacts-id/) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contact_lists/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-contact-lists-id/) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-surveys-id/) |
| [Get Survey Folder](actions/get-survey-folder.md) | `GET /survey_folders/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-survey-folders-id/) |
| [Get User](actions/get-user.md) | `GET /users/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-users-id/) |
| [List Audit Log Events](actions/list-audit-log-events.md) | `GET /audit_logs/events` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-audit-logs-events/) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /audit_logs` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-audit-logs/) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-channels/) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contact_lists` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-contact-lists/) |
| [List Contact Properties](actions/list-contact-properties.md) | `GET /contact_properties` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-contact-properties/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-contacts/) |
| [List Expressions](actions/list-expressions.md) | `GET /expressions` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-expressions/) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-languages/) |
| [List Questions](actions/list-questions.md) | `GET /questions` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-questions/) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-responses/) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-roles/) |
| [List Survey Folders](actions/list-survey-folders.md) | `GET /survey_folders` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-survey-folders/) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-surveys/) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-teams/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-users/) |
| [List Variables](actions/list-variables.md) | `GET /variables` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-variables/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.surveysparrow.com/rest-apis/get-v-3-webhooks/) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/put-v-3-contacts-id/) |
| [Update Contact List](actions/update-contact-list.md) | `PATCH /contact_lists/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/patch-v-3-contact-lists-id/) |
| [Update Contact Property](actions/update-contact-property.md) | `PATCH /contact_properties/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/patch-v-3-contact-properties-id/) |
| [Update Survey Folder](actions/update-survey-folder.md) | `PATCH /survey_folders/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/patch-v-3-survey-folders-id/) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/{{id}}` | [docs](https://developers.surveysparrow.com/rest-apis/put-v-3-webhooks-id/) |
