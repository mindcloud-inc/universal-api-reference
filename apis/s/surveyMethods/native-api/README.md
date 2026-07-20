# SurveyMethods: Native API Reference

A consolidated summary of SurveyMethods's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf
- **API base URL:** `https://api.surveymethods.com/v1`

## Authentication

### API Key

Authenticate to SurveyMethods with the account login ID and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Login ID:** `loginId` · required · SurveyMethods account login ID, usually the account email address.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf)

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
| [Get Response](actions/get-response.md) | `GET /:loginId/:apiKey/responses/:surveyCode/detail/:responseCode/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [Get Response Dashboard](actions/get-response-dashboard.md) | `GET /:loginId/:apiKey/responses/:surveyCode/dashboard/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [Get Response Question](actions/get-response-question.md) | `GET /:loginId/:apiKey/responses/:surveyCode/detail/:responseCode/:questionCode/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [Get Survey](actions/get-survey.md) | `GET /:loginId/:apiKey/surveys/:surveyCode/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [Get User Details](actions/get-user-details.md) | `GET /:loginId/:apiKey/users/details/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Completed Response Summaries](actions/list-completed-response-summaries.md) | `GET /:loginId/:apiKey/responses/:surveyCode/summary/completed/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Email List Contacts](actions/list-email-list-contacts.md) | `GET /:loginId/:apiKey/emaillists/:emailListCode/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Email Lists](actions/list-email-lists.md) | `GET /:loginId/:apiKey/emaillists/codes/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Email Response Summaries](actions/list-email-response-summaries.md) | `GET /:loginId/:apiKey/responses/:surveyCode/summary/email/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Master Opt-Out Emails](actions/list-master-opt-out-emails.md) | `GET /:loginId/:apiKey/emaillists/masteroptoutlist/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Newsletter Codes](actions/list-newsletter-codes.md) | `GET /:loginId/:apiKey/newsletters/codes/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Partial Response Summaries](actions/list-partial-response-summaries.md) | `GET /:loginId/:apiKey/responses/:surveyCode/summary/partial/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Response Codes](actions/list-response-codes.md) | `GET /:loginId/:apiKey/responses/:surveyCode/codes/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Response Summaries](actions/list-response-summaries.md) | `GET /:loginId/:apiKey/responses/:surveyCode/summary/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Survey Codes](actions/list-survey-codes.md) | `GET /:loginId/:apiKey/integrations/surveycodes/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Surveys](actions/list-surveys.md) | `GET /:loginId/:apiKey/surveys/details/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [List Web Response Summaries](actions/list-web-response-summaries.md) | `GET /:loginId/:apiKey/responses/:surveyCode/summary/web/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
| [Validate User](actions/validate-user.md) | `GET /:loginId/:apiKey/users/validate/` | [docs](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf) |
