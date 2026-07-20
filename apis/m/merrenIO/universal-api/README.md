# <img src="https://images.mindcloud.co/apps/icons/id-vve-bjs8m-1775587781298_1775587786575.jpeg" alt="MerrenIO logo" width="28" height="28"> MerrenIO: Universal API

Merren is an AI-powered customer research platform that supports customer feedback survey integrations through APIs, webhooks, and connected applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/merrenIO/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://merren.io
- **Vendor API docs:** https://merren.io/api-integration/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Filter Compare And Export Responses](actions/filter-compare-and-export-responses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/filter-compare-and-export-responses?connectionId=$CONNECTION_ID&type=question&surveyId=680000000000000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Carry Forward Question

| Action | Method | Description |
| --- | --- | --- |
| [Carry Forward Selected Answers](actions/carry-forward-selected-answers.md) | PUT |  |

### Facebook Messenger Deploy Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Facebook Messenger Deploy Link](actions/generate-facebook-messenger-deploy-link.md) | POST |  |

### Filtered Response Report

| Action | Method | Description |
| --- | --- | --- |
| [Filter Compare And Export Responses](actions/filter-compare-and-export-responses.md) | GET |  |

### Forced Carry Forward Question

| Action | Method | Description |
| --- | --- | --- |
| [Force Carry Forward Last Option](actions/force-carry-forward-last-option.md) | PUT |  |

### Insight Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Insight Data](actions/get-insight-data.md) | GET |  |

### Multi Choice Question

| Action | Method | Description |
| --- | --- | --- |
| [Configure Multi Choice Nominal Question](actions/configure-multi-choice-nominal-question.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Section](actions/add-section.md) | POST |  |
| [Add Survey Language Set](actions/add-survey-language-set.md) | PUT |  |
| [Build Question And Media Prompt Flow](actions/build-question-and-media-prompt-flow.md) | POST |  |
| [Change Survey Category](actions/change-survey-category.md) | PUT |  |
| [Clone Survey](actions/clone-survey.md) | POST |  |
| [Configure Repeat Response Rule](actions/configure-repeat-response-rule.md) | PUT |  |
| [Create Date Question](actions/create-date-question.md) | POST |  |
| [Create Media Message](actions/create-media-message.md) | POST |  |
| [Create Media Response Question](actions/create-media-response-question.md) | POST |  |
| [Create Nominal Question](actions/create-nominal-question.md) | POST |  |
| [Create Numeric Question](actions/create-numeric-question.md) | POST |  |
| [Create PII Email Question](actions/create-pii-email-question.md) | POST |  |
| [Create PII Telephone Question](actions/create-pii-telephone-question.md) | POST |  |
| [Create Ranking Question](actions/create-ranking-question.md) | POST |  |
| [Create Scale Question](actions/create-scale-question.md) | POST |  |
| [Create Survey From Scratch](actions/create-survey-from-scratch.md) | POST |  |
| [Create Survey From Template](actions/create-survey-from-template.md) | POST |  |
| [Create Survey With AI Builder](actions/create-survey-with-ai-builder.md) | POST |  |
| [Create Text Message](actions/create-text-message.md) | POST |  |
| [Create Text Question](actions/create-text-question.md) | POST |  |
| [Preview Survey Flow](actions/preview-survey-flow.md) | GET |  |
| [Rename Survey](actions/rename-survey.md) | PUT |  |

### Panel Respondent Source

| Action | Method | Description |
| --- | --- | --- |
| [Use Merren Panel To Source Respondents](actions/use-merren-panel-to-source-respondents.md) | POST |  |

### Randomized Question

| Action | Method | Description |
| --- | --- | --- |
| [Randomize Multiple Choice Options](actions/randomize-multiple-choice-options.md) | PUT |  |

### Response Summary Report

| Action | Method | Description |
| --- | --- | --- |
| [View Individual Table And Pie Chart Responses](actions/view-individual-table-and-pie-chart-responses.md) | GET |  |

### Single Choice Question

| Action | Method | Description |
| --- | --- | --- |
| [Configure Single Choice Nominal Question](actions/configure-single-choice-nominal-question.md) | PUT |  |

### Survey Language Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Prompt Respondent To Choose Language](actions/prompt-respondent-to-choose-language.md) | PUT |  |

### Translated Survey

| Action | Method | Description |
| --- | --- | --- |
| [Auto Translate Multilingual Survey](actions/auto-translate-multilingual-survey.md) | PUT |  |

### Translation Update

| Action | Method | Description |
| --- | --- | --- |
| [Manually Edit Translations](actions/manually-edit-translations.md) | PUT |  |

### Whatsapp Deploy Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate WhatsApp Deploy Link](actions/generate-whats-app-deploy-link.md) | POST |  |

### Whatsapp Push Csv Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload CSV For WhatsApp Push](actions/upload-csv-for-whats-app-push.md) | POST |  |

### Whatsapp Push Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Push Invitations](actions/send-whats-app-push-invitations.md) | POST |  |

