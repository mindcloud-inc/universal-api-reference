# <img src="https://images.mindcloud.co/apps/icons/question-pro-surveys_1774467904280.png" alt="QuestionPro Surveys logo" width="28" height="28"> QuestionPro Surveys: Universal API

Create, send, and analyze surveys and survey responses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/questionProSurveys/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.questionpro.com/enterprise-survey-software.html
- **Vendor API docs:** https://www.questionpro.com/api/getting-started.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get Answer](actions/get-answer.md) | GET |  |
| [Get Answers](actions/get-answers.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET |  |
| [Get Folders](actions/get-folders.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Image](actions/get-image.md) | GET |  |
| [Get Images](actions/get-images.md) | GET |  |
| [Get User Image](actions/get-user-image.md) | GET |  |
| [Get User Images](actions/get-user-images.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Question](actions/get-question.md) | GET |  |
| [Get Questions](actions/get-questions.md) | GET |  |

### Question Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Question Statistics](actions/get-question-statistics.md) | GET |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder Surveys](actions/get-folder-surveys.md) | GET |  |
| [Get Survey](actions/get-survey.md) | GET |  |
| [Get User Surveys](actions/get-user-surveys.md) | GET |  |

### Survey Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Authentication](actions/get-survey-authentication.md) | GET |  |

### Survey Block

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Block](actions/get-survey-block.md) | GET |  |
| [Get Survey Blocks](actions/get-survey-blocks.md) | GET |  |

### Survey Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response](actions/get-response.md) | GET |  |
| [Get Response Filter](actions/get-response-filter.md) | GET |  |
| [Get Responses](actions/get-responses.md) | GET |  |

### Survey Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Statistics](actions/get-survey-statistics.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get All Users from Organization](actions/get-all-users-from-organization.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [Search User](actions/search-user.md) | GET |  |

