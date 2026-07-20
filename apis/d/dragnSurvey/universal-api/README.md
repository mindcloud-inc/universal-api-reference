# <img src="https://images.mindcloud.co/apps/icons/f03218f6-a3f1-4649-bb2c-0c90362e6ec7_1774873475427.png" alt="Drag'n Survey logo" width="28" height="28"> Drag'n Survey: Universal API

Access Drag'n Survey surveys, collectors, respondents, reports, questions, and webhooks through the official Drag'n Survey REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dragnSurvey/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dragnsurvey.com
- **Vendor API docs:** https://developer.dragnsurvey.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Collector

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Collector](actions/create-survey-collector.md) | POST | Creates a collector for a Drag'n Survey survey. |
| [Delete Collector](actions/delete-collector.md) | DELETE | Deletes a collector from Drag'n Survey. |
| [Get Collector](actions/get-collector.md) | GET | Retrieves a collector from Drag'n Survey by ID. |
| [List Survey Collectors](actions/list-survey-collectors.md) | GET | Retrieves collectors for a Drag'n Survey survey. |
| [Update Collector](actions/update-collector.md) | PUT | Updates a collector in Drag'n Survey. |

### Collector Auth Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Collector Custom Links](actions/create-collector-custom-links.md) | POST | Creates respondent identification links for a Drag'n Survey collector. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Drag'n Survey by ID. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Question Definition](actions/get-question-definition.md) | GET | Retrieves a question definition from Drag'n Survey. |

### Question Response

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Question Responses](actions/retrieve-question-responses.md) | GET | Retrieves responses for a Drag'n Survey question. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Drag'n Survey by ID. |

### Respondent

| Action | Method | Description |
| --- | --- | --- |
| [Delete Respondent](actions/delete-respondent.md) | DELETE | Deletes a respondent from Drag'n Survey. |
| [Get Respondent Responses](actions/get-respondent-responses.md) | GET | Retrieves responses for a Drag'n Survey respondent. |

### Respondent Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Human Readable Respondent Responses](actions/get-human-readable-respondent-responses.md) | GET | Retrieves human-readable responses for a Drag'n Survey respondent. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves available surveys from Drag'n Survey. |

### Survey Respondent

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Respondent IDs](actions/list-survey-respondent-ids.md) | GET | Retrieves respondent IDs for a Drag'n Survey survey. |
| [List Survey Respondent IDs Paginated](actions/list-survey-respondent-ids-paginated.md) | GET | Retrieves paginated respondent IDs for a Drag'n Survey survey. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Drag'n Survey by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhooks from Drag'n Survey. |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | POST | Creates a webhook subscription in Drag'n Survey. |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | DELETE | Deletes a webhook from Drag'n Survey. |

