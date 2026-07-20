# <img src="https://images.mindcloud.co/apps/icons/smart-survey_1774377279356.png" alt="SmartSurvey logo" width="28" height="28"> SmartSurvey: Universal API

SmartSurvey API provides access to survey data, from listing all surveys to getting all the responses for a survey.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartSurvey/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smartsurvey.co.uk
- **Vendor API docs:** https://docs.smartsurvey.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Close Survey](actions/close-survey.md) | PUT | Closes a survey and its tracking links in SmartSurvey. |
| [Copy Survey](actions/copy-survey.md) | POST | Copies an existing survey in SmartSurvey. |
| [Create Survey](actions/create-survey.md) | POST | Creates a new survey in SmartSurvey. |
| [Delete Survey](actions/delete-survey.md) | DELETE | Deletes an existing survey from SmartSurvey. |
| [Get Survey](actions/get-survey.md) | GET | Retrieves a survey from your SmartSurvey account. |
| [Get Survey Details](actions/get-survey-details.md) | GET | Retrieves detailed survey information from SmartSurvey. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves all surveys in your SmartSurvey account. |
| [Open Survey](actions/open-survey.md) | PUT | Opens a survey's default tracking link in SmartSurvey. |
| [Print Survey](actions/print-survey.md) | GET | Renders a SmartSurvey survey as HTML, Word, or PDF. |
| [Update Survey Result Sharing](actions/update-survey-result-sharing.md) | PUT | Updates result sharing settings for a SmartSurvey survey. |

### Survey Export

| Action | Method | Description |
| --- | --- | --- |
| [Delete Survey Export](actions/delete-survey-export.md) | DELETE | Deletes an existing survey export from SmartSurvey. |
| [Download Latest Survey Export](actions/download-latest-survey-export.md) | GET | Downloads the latest survey export file from SmartSurvey. |
| [Download Latest Survey Export By Type](actions/download-latest-survey-export-by-type.md) | GET | Downloads the latest survey export file by type from SmartSurvey. |
| [Download Survey Export](actions/download-survey-export.md) | GET | Downloads a survey export file from SmartSurvey. |
| [Get Survey Export](actions/get-survey-export.md) | GET | Retrieves a survey export from SmartSurvey. |
| [List Survey Exports](actions/list-survey-exports.md) | GET | Retrieves all survey exports for a SmartSurvey survey. |
| [Replace Survey Export Emails](actions/replace-survey-export-emails.md) | PUT | Replaces email addresses in future scheduled survey exports in SmartSurvey. |

### Survey Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Folder](actions/create-survey-folder.md) | POST | Creates a new survey folder in SmartSurvey. |
| [Get Survey Folder](actions/get-survey-folder.md) | GET | Retrieves a survey folder from SmartSurvey. |
| [Get Survey Folder Details](actions/get-survey-folder-details.md) | GET | Retrieves a survey folder with its surveys from SmartSurvey. |
| [List Survey Folders](actions/list-survey-folders.md) | GET | Retrieves all survey folders from SmartSurvey. |

### Survey Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Invitation](actions/get-survey-invitation.md) | GET | Retrieves a survey invitation from SmartSurvey. |
| [List Survey Invitations](actions/list-survey-invitations.md) | GET | Retrieves survey invitations for a SmartSurvey survey. |
| [Send Survey Invitation](actions/send-survey-invitation.md) | POST | Sends a SmartSurvey invitation to one recipient. |
| [Send Survey Invitation Batch](actions/send-survey-invitation-batch.md) | POST | Sends a SmartSurvey invitation to multiple recipients. |

### Survey Invitation Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Invitation Fields](actions/get-survey-invitation-fields.md) | GET | Retrieves custom fields for a SmartSurvey invitation. |

### Survey Invitation Response

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Invitation Responses](actions/list-survey-invitation-responses.md) | GET | Retrieves responses for a SmartSurvey invitation. |

### Survey Owner

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Owner Information](actions/get-survey-owner-information.md) | GET | Retrieves survey owner information and metadata from SmartSurvey. |

### Survey Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Response](actions/get-survey-response.md) | GET | Retrieves a survey response from SmartSurvey. |
| [List Survey Responses](actions/list-survey-responses.md) | GET | Retrieves survey responses from a SmartSurvey survey. |

### Survey Tracking Link

| Action | Method | Description |
| --- | --- | --- |
| [Close Survey Tracking Link](actions/close-survey-tracking-link.md) | PUT | Closes a survey tracking link in SmartSurvey. |
| [Copy Survey Tracking Link](actions/copy-survey-tracking-link.md) | POST | Copies an existing survey tracking link in SmartSurvey. |
| [Create Survey Tracking Link](actions/create-survey-tracking-link.md) | POST | Creates a new survey tracking link in SmartSurvey. |
| [Delete Survey Tracking Link](actions/delete-survey-tracking-link.md) | DELETE | Deletes an existing survey tracking link from SmartSurvey. |
| [Get Survey Tracking Link](actions/get-survey-tracking-link.md) | GET | Retrieves a survey tracking link from SmartSurvey. |
| [List Survey Tracking Links](actions/list-survey-tracking-links.md) | GET | Retrieves tracking links for a SmartSurvey survey. |
| [Open Survey Tracking Link](actions/open-survey-tracking-link.md) | PUT | Opens a survey tracking link in SmartSurvey. |
| [Update Survey Tracking Link](actions/update-survey-tracking-link.md) | PUT | Updates an existing survey tracking link in SmartSurvey. |
| [Update Survey Tracking Link Auto Close Date](actions/update-survey-tracking-link-auto-close-date.md) | PUT | Updates a survey tracking link auto-close date in SmartSurvey. |
| [Update Survey Tracking Link Text](actions/update-survey-tracking-link-text.md) | PUT | Updates the text of a survey tracking link in SmartSurvey. |

