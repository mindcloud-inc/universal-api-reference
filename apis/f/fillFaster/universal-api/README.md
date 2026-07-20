# <img src="https://images.mindcloud.co/apps/icons/fillfaster-icon_1776183932162.png" alt="FillFaster logo" width="28" height="28"> FillFaster: Universal API

FillFaster API integration for forms, submissions, PDFs, and webhook management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fillFaster/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fillfaster.com
- **Vendor API docs:** https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | POST | Generates a filled PDF from a FillFaster form. |
| [Get Submission PDF](actions/get-submission-pdf.md) | GET | Retrieves a submission PDF from FillFaster by submission ID. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of active forms from FillFaster. |
| [Update Form Settings](actions/update-form-settings.md) | PUT | Updates settings for an existing form in FillFaster. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Submissions](actions/create-bulk-submissions.md) | POST | Creates multiple submissions in FillFaster. |
| [Create Submission Link](actions/create-submission-link.md) | POST | Creates a unique submission link in FillFaster. |
| [Get Form Fields](actions/get-form-fields.md) | GET | Retrieves form fields from FillFaster by form ID. |
| [Get Form Settings](actions/get-form-settings.md) | GET | Retrieves form settings from FillFaster by form ID. |
| [Get Submission Status](actions/get-submission-status.md) | GET | Retrieves submission status from FillFaster by submission ID. |
| [Get Submissions List](actions/get-submissions-list.md) | GET | Retrieves submissions for a specific FillFaster form. |
| [Subscribe Webhook](actions/subscribe-webhook.md) | POST | Subscribes a webhook URL to a FillFaster form. |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | DELETE | Removes a webhook URL from a FillFaster form. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in FillFaster. |

