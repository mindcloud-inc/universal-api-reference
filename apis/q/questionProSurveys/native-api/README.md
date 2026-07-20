# QuestionPro Surveys: Native API Reference

A consolidated summary of QuestionPro Surveys's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.questionpro.com/api/getting-started.html
- **API base URL:** `https://api.questionpro.com/a/api/v2`

## Authentication

### API Key

Authenticate QuestionPro Surveys API requests with an account API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.questionpro.com/api/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `response`. The total page count is read from `pagination.totalPages`. The current page number is read from `pagination.currentPage`.

## Pagination

Use `perPage` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Users from Organization](actions/get-all-users-from-organization.md) | `GET organizations/:organizationId/users` | [docs](https://www.questionpro.com/api/get-all-users-from-organization.html) |
| [Get Answer](actions/get-answer.md) | `GET surveys/:surveyId/questions/:questionId/answers/:answerId` | [docs](https://www.questionpro.com/api/get-answer.html) |
| [Get Answers](actions/get-answers.md) | `GET surveys/:surveyId/questions/:questionId/answers` | [docs](https://www.questionpro.com/api/get-answers.html) |
| [Get Folder](actions/get-folder.md) | `GET users/:userId/folders/:folderId` | [docs](https://www.questionpro.com/api/get-folder.html) |
| [Get Folder Surveys](actions/get-folder-surveys.md) | `GET users/:userId/folders/:folderId/surveys` | [docs](https://www.questionpro.com/api/get-folder-surveys.html) |
| [Get Folders](actions/get-folders.md) | `GET users/:userId/folders` | [docs](https://www.questionpro.com/api/get-folders.html) |
| [Get Image](actions/get-image.md) | `GET images/:imageId` | [docs](https://www.questionpro.com/api/get-image.html) |
| [Get Images](actions/get-images.md) | `GET images` | [docs](https://www.questionpro.com/api/get-images.html) |
| [Get Organization](actions/get-organization.md) | `GET organizations/:organizationId` | [docs](https://www.questionpro.com/api/get-organization.html) |
| [Get Question](actions/get-question.md) | `GET surveys/:surveyId/questions/:questionId` | [docs](https://www.questionpro.com/api/get-question.html) |
| [Get Question Statistics](actions/get-question-statistics.md) | `POST surveys/:surveyId/questions/:questionId/analytics` | [docs](https://www.questionpro.com/api/get-question-statistics.html) |
| [Get Questions](actions/get-questions.md) | `GET surveys/:surveyId/questions` | [docs](https://www.questionpro.com/api/get-questions.html) |
| [Get Response](actions/get-response.md) | `GET surveys/:surveyId/responses/:responseId` | [docs](https://www.questionpro.com/api/get-response.html) |
| [Get Response Filter](actions/get-response-filter.md) | `GET surveys/:surveyId/responses/filter` | [docs](https://www.questionpro.com/api/get-responses-filter.html) |
| [Get Responses](actions/get-responses.md) | `GET surveys/:surveyId/responses` | [docs](https://www.questionpro.com/api/get-responses.html) |
| [Get Survey](actions/get-survey.md) | `GET surveys/:surveyId` | [docs](https://www.questionpro.com/api/get-survey.html) |
| [Get Survey Authentication](actions/get-survey-authentication.md) | `GET surveys/:surveyId/authentication` | [docs](https://www.questionpro.com/api/get-survey-authentication.html) |
| [Get Survey Block](actions/get-survey-block.md) | `GET surveys/:surveyId/blocks/:blockId` | [docs](https://www.questionpro.com/api/get-survey-block.html) |
| [Get Survey Blocks](actions/get-survey-blocks.md) | `GET surveys/:surveyId/blocks` | [docs](https://www.questionpro.com/api/get-survey-blocks.html) |
| [Get Survey Statistics](actions/get-survey-statistics.md) | `POST surveys/:surveyId/analytics` | [docs](https://www.questionpro.com/api/get-survey-statistics.html) |
| [Get User](actions/get-user.md) | `GET users/:userId` | [docs](https://www.questionpro.com/api/get-user.html) |
| [Get User Image](actions/get-user-image.md) | `GET users/:userId/images/:imageId` | [docs](https://www.questionpro.com/api/get-user-image.html) |
| [Get User Images](actions/get-user-images.md) | `GET users/:userId/images` | [docs](https://www.questionpro.com/api/get-user-images.html) |
| [Get User Surveys](actions/get-user-surveys.md) | `GET users/:userId/surveys` | [docs](https://www.questionpro.com/api/get-user-surveys.html) |
| [Search User](actions/search-user.md) | `GET organizations/:organizationId/users/search` | [docs](https://www.questionpro.com/api/search-user.html) |
