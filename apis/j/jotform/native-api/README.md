# Jotform: Native API Reference

A consolidated summary of Jotform's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://api.jotform.com/docs/
- **API base URL:** `https://api.jotform.com`

## Authentication

### API Key

Use a Jotform API key generated from My Account > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.jotform.com/help/253-how-to-create-a-jotform-api-key/)

## API conventions

Response data is read from `content`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `lt`, `ne`.

## Sorting

Set the sort field with `orderby` in the query string. Only one sort field is accepted.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /user/forms` | [docs](https://api.jotform.com/docs/) |
| [Create Form Submission](actions/create-form-submission.md) | `POST /form/:formId/submissions` | [docs](https://api.jotform.com/docs/) |
| [Create Form Webhook](actions/create-form-webhook.md) | `POST /form/:formId/webhooks` | [docs](https://api.jotform.com/docs/) |
| [Delete Form](actions/delete-form.md) | `DELETE /form/:formId` | [docs](https://api.jotform.com/docs/) |
| [Delete Form Question](actions/delete-form-question.md) | `DELETE /form/:formId/question/:questionId` | [docs](https://api.jotform.com/docs/) |
| [Delete Form Webhook](actions/delete-form-webhook.md) | `DELETE /form/:formId/webhooks/:webhookId` | [docs](https://api.jotform.com/docs/) |
| [Delete Report](actions/delete-report.md) | `DELETE /report/:reportId` | [docs](https://api.jotform.com/docs/) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /submission/:submissionId` | [docs](https://api.jotform.com/docs/) |
| [Get Form](actions/get-form.md) | `GET /form/:formId` | [docs](https://api.jotform.com/docs/) |
| [Get Form Properties](actions/get-form-properties.md) | `GET /form/:formId/properties` | [docs](https://api.jotform.com/docs/) |
| [Get Form Property](actions/get-form-property.md) | `GET /form/:formId/properties/:propertyKey` | [docs](https://api.jotform.com/docs/) |
| [Get Form Question](actions/get-form-question.md) | `GET /form/:formId/question/:questionId` | [docs](https://api.jotform.com/docs/) |
| [Get Monthly Usage](actions/get-monthly-usage.md) | `GET /user/usage` | [docs](https://api.jotform.com/docs/#user-id-get-user-usage) |
| [Get Report](actions/get-report.md) | `GET /report/:reportId` | [docs](https://api.jotform.com/docs/) |
| [Get Submission](actions/get-submission.md) | `GET /submission/:submissionId` | [docs](https://api.jotform.com/docs/) |
| [Get System Plan](actions/get-system-plan.md) | `GET /system/plan/:planName` | [docs](https://api.jotform.com/docs/) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://api.jotform.com/docs/#user-id-get-user) |
| [Get User Setting By Key](actions/get-user-setting-by-key.md) | `GET /user/settings/:settingsKey` | [docs](https://api.jotform.com/docs/) |
| [Get User Settings](actions/get-user-settings.md) | `GET /user/settings` | [docs](https://api.jotform.com/docs/) |
| [List Form Questions](actions/list-form-questions.md) | `GET /form/:formId/questions` | [docs](https://api.jotform.com/docs/) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /form/:id/submissions` | [docs](https://api.jotform.com/docs/#form-id-get-form-submissions) |
| [List Form Uploads](actions/list-form-uploads.md) | `GET /form/:formId/files` | [docs](https://api.jotform.com/docs/) |
| [List Form Webhooks](actions/list-form-webhooks.md) | `GET /form/:formId/webhooks` | [docs](https://api.jotform.com/docs/) |
| [List Sub-User Accounts](actions/list-sub-user-accounts.md) | `GET /user/subusers` | [docs](https://api.jotform.com/docs/) |
| [List User Forms](actions/list-user-forms.md) | `GET /user/forms` | [docs](https://api.jotform.com/docs/#user-id-get-user-forms) |
| [List User History](actions/list-user-history.md) | `GET /user/history` | [docs](https://api.jotform.com/docs/) |
| [List User Invoices](actions/list-user-invoices.md) | `GET /user/invoices` | [docs](https://api.jotform.com/docs/) |
| [List User Reports](actions/list-user-reports.md) | `GET /user/reports` | [docs](https://api.jotform.com/docs/) |
| [List User Submissions](actions/list-user-submissions.md) | `GET /user/submissions` | [docs](https://api.jotform.com/docs/#user-id-get-user-submissions) |
| [Login User](actions/login-user.md) | `POST /user/login` | [docs](https://api.jotform.com/docs/#user-id-login-user) |
| [Logout User](actions/logout-user.md) | `GET /user/logout` | [docs](https://api.jotform.com/docs/) |
| [Register User](actions/register-user.md) | `POST /user/register` | [docs](https://api.jotform.com/docs/#user-id-register-user) |
| [Update User Settings](actions/update-user-settings.md) | `POST /user/settings` | [docs](https://api.jotform.com/docs/) |
