# Common Ninja: Native API Reference

A consolidated summary of Common Ninja's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://developers.commoninja.com/docs/intro
- **API base URL:** `https://api.commoninja.com/platform/api/v1`

## Authentication

### Account API Key

Common Ninja account-level API key from the account page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
CN-API-Token: <apiKey>
```

[Official authentication documentation](https://help.commoninja.com/hc/en-us/articles/21742833539613-How-to-Obtain-Your-Account-Level-API-Key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Widget](actions/create-widget.md) | `POST /widgets` | [docs](https://developers.commoninja.com/docs/api/widgets/widget-create) |
| [Delete Widget](actions/delete-widget.md) | `DELETE /widgets/:id` | [docs](https://developers.commoninja.com/docs/api/widgets/widget-delete) |
| [Get Contact](actions/get-contact.md) | `GET /projects/:projectId/contacts/:contactId` | [docs](https://developers.commoninja.com/docs/api/crm/contact) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://developers.commoninja.com/docs/api/projects/project) |
| [Get Submission](actions/get-submission.md) | `GET /projects/:projectId/submissions/:submissionId` | [docs](https://developers.commoninja.com/docs/api/crm/submission) |
| [Get User Details](actions/get-user-details.md) | `GET /user` | [docs](https://developers.commoninja.com/docs/api/user/user-details) |
| [Get Widget](actions/get-widget.md) | `GET /widgets/:id` | [docs](https://developers.commoninja.com/docs/api/widgets/widget) |
| [Get Widget Analytics](actions/get-widget-analytics.md) | `GET /widgets/:id/analytics` | [docs](https://developers.commoninja.com/docs/api/analytics/widget-analytics) |
| [Get Widget Editor URL](actions/get-widget-editor-url.md) | `GET /widgets/:id/editor` | [docs](https://developers.commoninja.com/docs/api/widgets/widget-editor) |
| [Get Widget Embed Code](actions/get-widget-embed-code.md) | `GET /widgets/:id/embed-code` | [docs](https://developers.commoninja.com/docs/api/widgets/widget-embed-code) |
| [Get Widget Type](actions/get-widget-type.md) | `GET /widget-types/:id` | [docs](https://developers.commoninja.com/docs/api/widget-types/widget-type) |
| [Get Widget Type Schema](actions/get-widget-type-schema.md) | `GET /widget-types/:id/schema` | [docs](https://developers.commoninja.com/docs/api/widget-types/widget-type-schema) |
| [List Contacts](actions/list-contacts.md) | `GET /projects/:projectId/contacts` | [docs](https://developers.commoninja.com/docs/api/crm/contacts-list) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.commoninja.com/docs/api/projects/projects-list) |
| [List Submissions](actions/list-submissions.md) | `GET /projects/:projectId/submissions` | [docs](https://developers.commoninja.com/docs/api/crm/submissions-list) |
| [List Widget Types](actions/list-widget-types.md) | `GET /widget-types` | [docs](https://developers.commoninja.com/docs/api/widget-types/widget-types-list) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://developers.commoninja.com/docs/api/widgets/widgets-list) |
| [Update Widget](actions/update-widget.md) | `PUT /widgets/:id` | [docs](https://developers.commoninja.com/docs/api/widgets/widget-update) |
