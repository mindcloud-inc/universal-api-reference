# <img src="https://images.mindcloud.co/apps/icons/jotform_1772465185334.png" alt="Jotform logo" width="28" height="28"> Jotform: Universal API

Build forms, collect submissions, accept payments, and manage responses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jotform/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jotform.com
- **Vendor API docs:** https://api.jotform.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Form Uploads](actions/list-form-uploads.md) | GET | Retrieves uploaded files for a Jotform form. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a form in Jotform. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from Jotform. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Jotform. |
| [List User Forms](actions/list-user-forms.md) | GET | Retrieves forms for the current Jotform user. |

### History

| Action | Method | Description |
| --- | --- | --- |
| [List User History](actions/list-user-history.md) | GET | Retrieves user history entries from Jotform. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List User Invoices](actions/list-user-invoices.md) | GET | Retrieves user invoice records from Jotform. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get System Plan](actions/get-system-plan.md) | GET | Retrieves a system plan from Jotform. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Properties](actions/get-form-properties.md) | GET | Retrieves properties for a Jotform form. |
| [Get Form Property](actions/get-form-property.md) | GET | Retrieves a form property from Jotform. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form Question](actions/delete-form-question.md) | DELETE | Deletes an existing form question from Jotform. |
| [Get Form Question](actions/get-form-question.md) | GET | Retrieves a form question from Jotform. |
| [List Form Questions](actions/list-form-questions.md) | GET | Retrieves questions for a Jotform form. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Delete Report](actions/delete-report.md) | DELETE | Deletes an existing report from Jotform. |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Jotform. |
| [List User Reports](actions/list-user-reports.md) | GET | Retrieves reports for the current Jotform user. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Login User](actions/login-user.md) | POST | Creates a user session in Jotform. |
| [Logout User](actions/logout-user.md) | DELETE | Ends a user session in Jotform. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get User Setting By Key](actions/get-user-setting-by-key.md) | GET | Retrieves a user setting from Jotform. |
| [Get User Settings](actions/get-user-settings.md) | GET | Retrieves user settings from Jotform. |
| [Update User Settings](actions/update-user-settings.md) | POST | Updates existing user settings in Jotform. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Submission](actions/create-form-submission.md) | POST | Creates a form submission in Jotform. |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from Jotform. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a submission from Jotform. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves submissions for a Jotform form. |
| [List User Submissions](actions/list-user-submissions.md) | GET | Retrieves user submissions from Jotform. |

### Subuser

| Action | Method | Description |
| --- | --- | --- |
| [List Sub-User Accounts](actions/list-sub-user-accounts.md) | GET | Retrieves sub-user accounts from Jotform. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Usage](actions/get-monthly-usage.md) | GET | Retrieves monthly usage details from Jotform. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from Jotform. |
| [Register User](actions/register-user.md) | POST | Registers a new user in Jotform. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Webhook](actions/create-form-webhook.md) | POST | Creates a webhook for a Jotform form. |
| [Delete Form Webhook](actions/delete-form-webhook.md) | DELETE | Deletes an existing form webhook from Jotform. |
| [List Form Webhooks](actions/list-form-webhooks.md) | GET | Retrieves webhooks for a Jotform form. |

