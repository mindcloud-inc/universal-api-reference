# <img src="https://images.mindcloud.co/apps/icons/images-12_1774630317234.jpeg" alt="Startquestion logo" width="28" height="28"> Startquestion: Universal API

Startquestion is a survey and form platform for creating surveys, forms, tests, and collecting and analyzing responses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/startquestion/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.startquestion.com
- **Vendor API docs:** https://help.startquestion.com/en/collections/3120305-api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Result Attachment](actions/download-result-attachment.md) | GET | Downloads a survey response attachment from Startquestion. |

### Batch Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Mailing](actions/create-batch-mailing.md) | POST | Creates a survey mailing from a respondent batch in Startquestion. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Startquestion. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Startquestion. |
| [Search Contacts](actions/search-contacts.md) | GET | Searches contacts in Startquestion. |

### Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing](actions/create-mailing.md) | POST | Creates a survey mailing in Startquestion. |

### Mailing Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Mailing Templates](actions/list-mailing-templates.md) | GET | Retrieves mailing templates from Startquestion. |

### Offline Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Offline Contact](actions/create-offline-contact.md) | POST | Creates a contact in Startquestion for offline distribution. |

### Questions

| Action | Method | Description |
| --- | --- | --- |
| [List Page Questions](actions/list-page-questions.md) | GET | Retrieves questions for a Startquestion survey page. |

### Respondent

| Action | Method | Description |
| --- | --- | --- |
| [Add Respondent to Survey](actions/add-respondent-to-survey.md) | POST | Adds a respondent to a Startquestion survey. |
| [Delete Respondent](actions/delete-respondent.md) | DELETE | Deletes a respondent from a Startquestion survey. |

### Respondent Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Respondent Batch](actions/create-respondent-batch.md) | POST | Creates a respondent batch for a Startquestion survey. |
| [Get Respondent Batch](actions/get-respondent-batch.md) | GET | Retrieves a Startquestion respondent batch by ID. |

### Respondent Patch

| Action | Method | Description |
| --- | --- | --- |
| [Append Respondent Batch](actions/append-respondent-batch.md) | POST | Adds respondents to a Startquestion batch. |
| [Get Respondent Patch](actions/get-respondent-patch.md) | GET | Retrieves a Startquestion respondent patch by ID. |

### Respondents

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Respondents](actions/list-survey-respondents.md) | GET | Retrieves respondents for a Startquestion survey. |
| [Search Survey Respondents](actions/search-survey-respondents.md) | GET | Searches respondents in a Startquestion survey. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response V2 by ID](actions/get-response-v2-by-id.md) | GET | Retrieves a survey response from Startquestion by response ID with the v2 results format. |
| [Get Response V2 by Token](actions/get-response-v2-by-token.md) | GET | Retrieves a survey response from Startquestion by token with the v2 results format. |
| [Get Response V3 by ID](actions/get-response-v3-by-id.md) | GET | Retrieves a survey response from Startquestion by response ID with the v3 results format. |
| [Get Response V3 by Token](actions/get-response-v3-by-token.md) | GET | Retrieves a survey response from Startquestion by token with the v3 results format. |

### Responses

| Action | Method | Description |
| --- | --- | --- |
| [List Responses V2](actions/list-responses-v2.md) | GET | Retrieves survey responses from Startquestion with the v2 results format. |
| [List Responses V3](actions/list-responses-v3.md) | GET | Retrieves survey responses from Startquestion with the v3 results format. |
| [Search Responses by External Key](actions/search-responses-by-external-key.md) | GET | Retrieves survey responses from Startquestion by external key. |

### Result Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Result Metadata by Response ID](actions/get-result-metadata-by-response-id.md) | GET | Retrieves survey results metadata from Startquestion by response ID. |
| [Get Result Metadata by Token](actions/get-result-metadata-by-token.md) | GET | Retrieves survey results metadata from Startquestion by token. |
| [Get Results Metadata](actions/get-results-metadata.md) | GET | Retrieves survey results metadata from Startquestion. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET | Retrieves a survey from Startquestion by ID. |

### Surveys

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from Startquestion. |
| [Search Surveys](actions/search-surveys.md) | GET | Searches surveys in Startquestion. |

