# <img src="https://images.mindcloud.co/apps/icons/survicate_1774025396883.png" alt="Survicate logo" width="28" height="28"> Survicate: Universal API

Access Survicate Data Export API surveys, responses, respondents, and personal-data endpoints from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/survicate/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://survicate.com/
- **Vendor API docs:** https://developers.survicate.com/data-export/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Personal Data

| Action | Method | Description |
| --- | --- | --- |
| [Delete Personal Data By Email](actions/delete-personal-data-by-email.md) | DELETE | Deletes personal data by email from Survicate. |
| [Get Personal Data Counters](actions/get-personal-data-counters.md) | GET | Retrieves personal data counts by email from Survicate. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Questions](actions/list-survey-questions.md) | GET | Retrieves questions from a specific Survicate survey. |

### Respondent Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Respondent Attributes](actions/list-respondent-attributes.md) | GET | Retrieves attributes for a specific Survicate respondent. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response](actions/get-response.md) | GET | Retrieves a specific survey response from Survicate. |
| [List Respondent Responses](actions/list-respondent-responses.md) | GET | Retrieves responses from a specific Survicate respondent. |
| [List Survey Responses](actions/list-survey-responses.md) | GET | Retrieves responses for a specific Survicate survey. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET | Retrieves a specific survey from Survicate. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from your Survicate workspace. |

