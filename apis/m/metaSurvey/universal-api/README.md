# <img src="https://images.mindcloud.co/apps/icons/e-wcj8gwent-ccoyzo-exe-qdclhf4_1776820853425.png" alt="MetaSurvey logo" width="28" height="28"> MetaSurvey: Universal API

Create interactive card-style surveys for feedback collection and lead generation, with embeds, automations, and response tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/metaSurvey/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getmetasurvey.com/
- **Vendor API docs:** https://getmetasurvey.com/help

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metaSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Responses](actions/list-survey-responses.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey](actions/create-survey.md) | POST |  |
| [Delete Survey](actions/delete-survey.md) | DELETE |  |
| [Duplicate Survey](actions/duplicate-survey.md) | POST |  |
| [Get Survey](actions/get-survey.md) | GET |  |
| [Publish Survey](actions/publish-survey.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Question Choice](actions/create-question-choice.md) | POST |  |
| [Create Survey Question](actions/create-survey-question.md) | POST |  |
| [Delete Question Choice](actions/delete-question-choice.md) | DELETE |  |
| [Delete Survey Question](actions/delete-survey-question.md) | DELETE |  |
| [Duplicate Survey Question](actions/duplicate-survey-question.md) | POST |  |
| [List Survey Questions](actions/list-survey-questions.md) | GET |  |
| [Update Question Choice](actions/update-question-choice.md) | PUT |  |
| [Update Survey Question](actions/update-survey-question.md) | PUT |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET |  |

