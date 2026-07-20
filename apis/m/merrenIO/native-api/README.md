# MerrenIO: Native API Reference

A consolidated summary of MerrenIO's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://merren.io/api-integration/
- **API base URL:** `https://app.merren.io`

## Authentication

### Customer Session

Creates a Merren session from a customer-specific credential pair before calling protected survey endpoints.

### Credentials

- **Customer ID:** `customerId` · required · The Merren customer identifier used when creating a session.
- **Secret Code:** `secretCode` · required · The Merren secret code paired with the customer ID when creating a session.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://merren.io/api-integration/)

### Bearer Token

Uses a Merren bearer JWT from the login/signup flow for protected survey-builder endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.merren.io/accounts/login)

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Section](actions/add-section.md) | `POST /section/save` | [docs](https://merren.io/api-integration/) |
| [Add Survey Language Set](actions/add-survey-language-set.md) | `POST /survey/update` | [docs](https://merren.io/api-integration/) |
| [Auto Translate Multilingual Survey](actions/auto-translate-multilingual-survey.md) | `POST /survey/checkAllowTranslation` | [docs](https://merren.io/api-integration/) |
| [Build Question And Media Prompt Flow](actions/build-question-and-media-prompt-flow.md) | `POST /question/applyLogic` | [docs](https://merren.io/api-integration/) |
| [Carry Forward Selected Answers](actions/carry-forward-selected-answers.md) | `POST /question/updateQuestion` | [docs](https://merren.io/api-integration/) |
| [Change Survey Category](actions/change-survey-category.md) | `POST /survey/update` | [docs](https://merren.io/api-integration/) |
| [Clone Survey](actions/clone-survey.md) | `POST /survey/cloneSurvey` | [docs](https://merren.io/api-integration/) |
| [Configure Multi Choice Nominal Question](actions/configure-multi-choice-nominal-question.md) | `POST /question/updateQuestion` | [docs](https://merren.io/api-integration/) |
| [Configure Repeat Response Rule](actions/configure-repeat-response-rule.md) | `POST /survey/saveRecurringSurveyDetails` | [docs](https://merren.io/api-integration/) |
| [Configure Single Choice Nominal Question](actions/configure-single-choice-nominal-question.md) | `POST /question/updateQuestion` | [docs](https://merren.io/api-integration/) |
| [Create Date Question](actions/create-date-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Media Message](actions/create-media-message.md) | `POST /question/addMessage` | [docs](https://merren.io/api-integration/) |
| [Create Media Response Question](actions/create-media-response-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Nominal Question](actions/create-nominal-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Numeric Question](actions/create-numeric-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create PII Email Question](actions/create-pii-email-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create PII Telephone Question](actions/create-pii-telephone-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Ranking Question](actions/create-ranking-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Scale Question](actions/create-scale-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Create Survey From Scratch](actions/create-survey-from-scratch.md) | `POST /survey/create` | [docs](https://merren.io/api-integration/) |
| [Create Survey From Template](actions/create-survey-from-template.md) | `POST /survey/cloneSurveyTemplate` | [docs](https://merren.io/api-integration/) |
| [Create Survey With AI Builder](actions/create-survey-with-ai-builder.md) | `POST /generateSurvey/generateSurvey` | [docs](https://merren.io/api-integration/) |
| [Create Text Message](actions/create-text-message.md) | `POST /question/addMessage` | [docs](https://merren.io/api-integration/) |
| [Create Text Question](actions/create-text-question.md) | `POST /question/save` | [docs](https://merren.io/api-integration/) |
| [Filter Compare And Export Responses](actions/filter-compare-and-export-responses.md) | `POST /survey/comparisionByQuestion` | [docs](https://merren.io/api-integration/) |
| [Force Carry Forward Last Option](actions/force-carry-forward-last-option.md) | `POST /question/updateQuestion` | [docs](https://merren.io/api-integration/) |
| [Generate Facebook Messenger Deploy Link](actions/generate-facebook-messenger-deploy-link.md) | `POST /deploy/createSurveyLink/:surveyId` | [docs](https://merren.io/api-integration/) |
| [Generate WhatsApp Deploy Link](actions/generate-whats-app-deploy-link.md) | `POST /deploy/createSurveyLink/:surveyId` | [docs](https://merren.io/api-integration/) |
| [Get Insight Data](actions/get-insight-data.md) | `GET /auth/getInsightData` | [docs](https://merren.io/api-integration/) |
| [Manually Edit Translations](actions/manually-edit-translations.md) | `POST /question/updateTranslationQustion` | [docs](https://merren.io/api-integration/) |
| [Preview Survey Flow](actions/preview-survey-flow.md) | `POST /deploy/createPreviewAndTestSurveyLink/{surveyId}` | [docs](https://merren.io/api-integration/) |
| [Prompt Respondent To Choose Language](actions/prompt-respondent-to-choose-language.md) | `GET /survey/getSurveyLanguages` | [docs](https://merren.io/api-integration/) |
| [Randomize Multiple Choice Options](actions/randomize-multiple-choice-options.md) | `POST /question/updateQuestion` | [docs](https://merren.io/api-integration/) |
| [Rename Survey](actions/rename-survey.md) | `POST /survey/update` | [docs](https://merren.io/api-integration/) |
| [Send WhatsApp Push Invitations](actions/send-whats-app-push-invitations.md) | `POST /deploy/uploadRecipent` | [docs](https://merren.io/api-integration/) |
| [Upload CSV For WhatsApp Push](actions/upload-csv-for-whats-app-push.md) | `POST /deploy/uploadRecipients` | [docs](https://merren.io/api-integration/) |
| [Use Merren Panel To Source Respondents](actions/use-merren-panel-to-source-respondents.md) | `GET /deploy/getOnGoingSurveys/:surveyId` | [docs](https://merren.io/api-integration/) |
| [View Individual Table And Pie Chart Responses](actions/view-individual-table-and-pie-chart-responses.md) | `GET /survey/getQuestionSummary/:surveyId` | [docs](https://merren.io/api-integration/) |
