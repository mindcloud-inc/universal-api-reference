# MetaSurvey: Native API Reference

A consolidated summary of MetaSurvey's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://getmetasurvey.com/help
- **API base URL:** `https://api.getmetasurvey.com/api`

## Authentication

### Access Token

Authenticate with a current MetaSurvey bearer access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://getmetasurvey.com/help)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /admin/folder` |  |
| [Create Question Choice](actions/create-question-choice.md) | `POST /admin/survey/:surveyId/question/:questionId/choice` |  |
| [Create Survey](actions/create-survey.md) | `POST /admin/survey` |  |
| [Create Survey Question](actions/create-survey-question.md) | `POST /admin/survey/:surveyId/question` |  |
| [Delete Folder](actions/delete-folder.md) | `DELETE /admin/folder/:folderId` |  |
| [Delete Question Choice](actions/delete-question-choice.md) | `DELETE /admin/survey/:surveyId/question/:questionId/choice/:choiceId` |  |
| [Delete Survey](actions/delete-survey.md) | `DELETE /admin/survey/:surveyId` |  |
| [Delete Survey Question](actions/delete-survey-question.md) | `DELETE /admin/survey/:surveyId/question/:questionId` |  |
| [Duplicate Survey](actions/duplicate-survey.md) | `POST /admin/survey/:surveyId/duplicate` |  |
| [Duplicate Survey Question](actions/duplicate-survey-question.md) | `POST /admin/survey/:surveyId/question/:questionId/duplicate` |  |
| [Get Folder](actions/get-folder.md) | `GET /admin/folder/:folderId` |  |
| [Get Survey](actions/get-survey.md) | `GET /admin/survey/:surveyId` |  |
| [List Folders](actions/list-folders.md) | `GET /admin/folders` |  |
| [List Survey Questions](actions/list-survey-questions.md) | `GET /admin/survey/:surveyId/questions` |  |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /admin/survey/:surveyId/responses` |  |
| [List Surveys](actions/list-surveys.md) | `GET /admin/surveys` | [docs](https://getmetasurvey.com/help) |
| [Publish Survey](actions/publish-survey.md) | `POST /admin/survey/:surveyId/publish` |  |
| [Update Folder](actions/update-folder.md) | `PATCH /admin/folder/:folderId` |  |
| [Update Question Choice](actions/update-question-choice.md) | `PATCH /admin/survey/:surveyId/question/:questionId/choice/:choiceId` |  |
| [Update Survey Question](actions/update-survey-question.md) | `PATCH /admin/survey/:surveyId/question/:questionId` |  |
