# SmartSurvey: Native API Reference

A consolidated summary of SmartSurvey's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.smartsurvey.io/reference
- **API base URL:** `https://api.smartsurvey.io/v2`

## Authentication

### Basic

Use your SmartSurvey API Key as the username and your API Key Secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.smartsurvey.io/docs/getting-started#authentication)

## API conventions

The total page count is read from `pages`. The current page number is read from `page_index`.

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Multiple sort fields can be combined.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Survey](actions/close-survey.md) | `PATCH /surveys/{surveyId}/close` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-close) |
| [Close Survey Tracking Link](actions/close-survey-tracking-link.md) | `PATCH /surveys/{surveyId}/links/{id}/close` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-close) |
| [Copy Survey](actions/copy-survey.md) | `PUT /surveys/{surveyId}` | [docs](https://docs.smartsurvey.io/reference/put_surveys-surveyid) |
| [Copy Survey Tracking Link](actions/copy-survey-tracking-link.md) | `PUT /surveys/{surveyId}/links/{id}/copy` | [docs](https://docs.smartsurvey.io/reference/put_surveys-surveyid-links-id-copy) |
| [Create Survey](actions/create-survey.md) | `POST /surveys` | [docs](https://docs.smartsurvey.io/reference/post_surveys) |
| [Create Survey Folder](actions/create-survey-folder.md) | `POST /surveyfolders` | [docs](https://docs.smartsurvey.io/reference/post_surveyfolders) |
| [Create Survey Tracking Link](actions/create-survey-tracking-link.md) | `POST /surveys/{surveyId}/links` | [docs](https://docs.smartsurvey.io/reference/post_surveys-surveyid-links) |
| [Delete Survey](actions/delete-survey.md) | `DELETE /surveys/{surveyId}` | [docs](https://docs.smartsurvey.io/reference/delete_surveys-surveyid) |
| [Delete Survey Export](actions/delete-survey-export.md) | `DELETE /surveys/{surveyId}/exports/{surveyExportId}` | [docs](https://docs.smartsurvey.io/reference/delete_surveys-surveyid-exports-surveyexportid) |
| [Delete Survey Tracking Link](actions/delete-survey-tracking-link.md) | `DELETE /surveys/{surveyId}/links/{id}` | [docs](https://docs.smartsurvey.io/reference/delete_surveys-surveyid-links-id) |
| [Download Latest Survey Export](actions/download-latest-survey-export.md) | `GET /surveys/{surveyId}/exports/latest/download` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-latest-download) |
| [Download Latest Survey Export By Type](actions/download-latest-survey-export-by-type.md) | `GET /surveys/{surveyId}/exports/latest/download/{reportType}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-latest-download-reporttype) |
| [Download Survey Export](actions/download-survey-export.md) | `GET /surveys/{surveyId}/exports/{reportId}/download` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-reportid-download) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/{surveyId}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid) |
| [Get Survey Details](actions/get-survey-details.md) | `GET /surveys/{surveyId}/detailed` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-detailed) |
| [Get Survey Export](actions/get-survey-export.md) | `GET /surveys/{surveyId}/exports/{surveyExportId}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-surveyexportid) |
| [Get Survey Folder](actions/get-survey-folder.md) | `GET /surveyfolders/{id}` | [docs](https://docs.smartsurvey.io/reference/get_surveyfolders-id) |
| [Get Survey Folder Details](actions/get-survey-folder-details.md) | `GET /surveyfolders/{id}/detailed` | [docs](https://docs.smartsurvey.io/reference/get_surveyfolders-id-detailed) |
| [Get Survey Invitation](actions/get-survey-invitation.md) | `GET /surveys/{surveyId}/invitations/{invitationId}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid) |
| [Get Survey Invitation Fields](actions/get-survey-invitation-fields.md) | `GET /surveys/{surveyId}/invitations/{invitationId}/fields` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid-fields) |
| [Get Survey Owner Information](actions/get-survey-owner-information.md) | `GET /surveys/{surveyId}/ownerinfo` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-ownerinfo) |
| [Get Survey Response](actions/get-survey-response.md) | `GET /surveys/{surveyId}/responses/{responseId}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-responses-responseid) |
| [Get Survey Tracking Link](actions/get-survey-tracking-link.md) | `GET /surveys/{surveyId}/links/{id}` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-links-id) |
| [List Survey Exports](actions/list-survey-exports.md) | `GET /surveys/{surveyId}/exports` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports) |
| [List Survey Folders](actions/list-survey-folders.md) | `GET /surveyfolders` | [docs](https://docs.smartsurvey.io/reference/get_surveyfolders) |
| [List Survey Invitation Responses](actions/list-survey-invitation-responses.md) | `GET /surveys/{surveyId}/invitations/{invitationId}/list` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations-invitationid-list) |
| [List Survey Invitations](actions/list-survey-invitations.md) | `GET /surveys/{surveyId}/invitations` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-invitations) |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /surveys/{surveyId}/responses` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-responses) |
| [List Survey Tracking Links](actions/list-survey-tracking-links.md) | `GET /surveys/{surveyId}/links` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-links) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://docs.smartsurvey.io/reference/get_surveys) |
| [Open Survey](actions/open-survey.md) | `PATCH /surveys/{surveyId}/open` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-open) |
| [Open Survey Tracking Link](actions/open-survey-tracking-link.md) | `PATCH /surveys/{surveyId}/links/{id}/open` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-open) |
| [Print Survey](actions/print-survey.md) | `GET /surveys/{surveyId}/print` | [docs](https://docs.smartsurvey.io/reference/get_surveys-surveyid-print) |
| [Replace Survey Export Emails](actions/replace-survey-export-emails.md) | `POST /surveys/{surveyId}/exports/replace-emails` | [docs](https://docs.smartsurvey.io/reference/post_surveys-surveyid-exports-replace-emails) |
| [Send Survey Invitation](actions/send-survey-invitation.md) | `POST /surveys/{surveyId}/invitations/{invitationId}/sendone` | [docs](https://docs.smartsurvey.io/reference/post_surveys-surveyid-invitations-invitationid-sendone) |
| [Send Survey Invitation Batch](actions/send-survey-invitation-batch.md) | `POST /surveys/{surveyId}/invitations/{invitationId}/send` | [docs](https://docs.smartsurvey.io/reference/post_surveys-surveyid-invitations-invitationid-send) |
| [Update Survey Result Sharing](actions/update-survey-result-sharing.md) | `PATCH /surveys/{surveyId}/resultsharing` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-resultsharing) |
| [Update Survey Tracking Link](actions/update-survey-tracking-link.md) | `PUT /surveys/{surveyId}/links/{id}` | [docs](https://docs.smartsurvey.io/reference/put_surveys-surveyid-links-id) |
| [Update Survey Tracking Link Auto Close Date](actions/update-survey-tracking-link-auto-close-date.md) | `PATCH /surveys/{surveyId}/links/{id}/autoclosedate` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-autoclosedate) |
| [Update Survey Tracking Link Text](actions/update-survey-tracking-link-text.md) | `PATCH /surveys/{surveyId}/links/{id}/linktext` | [docs](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-linktext) |
