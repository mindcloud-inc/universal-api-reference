# <img src="https://images.mindcloud.co/apps/icons/idj-qzmq4e-b-1774468515981_1774468528191.jpeg" alt="Evalandgo logo" width="28" height="28"> Evalandgo: Universal API

Create surveys, collect responses, and analyze questionnaire results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evalandgo/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.evalandgo.com
- **Vendor API docs:** https://app.evalandgo.com/api/docs/v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Evalandgo. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Evalandgo. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Evalandgo. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from Evalandgo. |

### Form Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Response](actions/create-form-response.md) | POST | Creates a form response in Evalandgo. |
| [Retrieve Form Response](actions/retrieve-form-response.md) | GET | Retrieves a form response from Evalandgo. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Form Question](actions/retrieve-form-question.md) | GET | Retrieves a form question from Evalandgo. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Evalandgo. |
| [Retrieve Group](actions/retrieve-group.md) | GET | Retrieves a group from Evalandgo. |

### Multiple Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Response](actions/create-multiple-response.md) | POST | Creates a multiple response in Evalandgo. |
| [Update Multiple Response](actions/update-multiple-response.md) | PUT | Updates an existing multiple response in Evalandgo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Questionnaire Questions](actions/list-questionnaire-questions.md) | GET | Retrieves questions for a questionnaire from Evalandgo. |

### Question Drawing File

| Action | Method | Description |
| --- | --- | --- |
| [Download Question Drawing Files](actions/download-question-drawing-files.md) | GET | Retrieves drawing files for a question from Evalandgo. |

### Question Upload File

| Action | Method | Description |
| --- | --- | --- |
| [Download Question Upload Files](actions/download-question-upload-files.md) | GET | Retrieves uploaded files for a question from Evalandgo. |

### Questionnaire

| Action | Method | Description |
| --- | --- | --- |
| [List Questionnaires](actions/list-questionnaires.md) | GET | Retrieves questionnaires from Evalandgo. |
| [Retrieve Questionnaire](actions/retrieve-questionnaire.md) | GET | Retrieves a questionnaire from Evalandgo. |

### Respondent

| Action | Method | Description |
| --- | --- | --- |
| [Create Respondent](actions/create-respondent.md) | POST | Creates a new respondent in Evalandgo. |
| [List Contact Respondents](actions/list-contact-respondents.md) | GET | Retrieves respondents for a contact from Evalandgo. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Question Responses](actions/list-question-responses.md) | GET | Retrieves responses for a question from Evalandgo. |
| [List Respondent Responses](actions/list-respondent-responses.md) | GET | Retrieves responses for a respondent from Evalandgo. |
| [Retrieve Respondent Response](actions/retrieve-respondent-response.md) | GET | Retrieves a response for a respondent from Evalandgo. |

### Response Input

| Action | Method | Description |
| --- | --- | --- |
| [Update Form Response Input](actions/update-form-response-input.md) | PUT | Updates an input in a form response in Evalandgo. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Evalandgo. |

### Text Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Text Response](actions/create-text-response.md) | POST | Creates a text response in Evalandgo. |
| [Update Text Response](actions/update-text-response.md) | PUT | Updates an existing text response in Evalandgo. |

### Unique Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Unique Response](actions/create-unique-response.md) | POST | Creates a unique response in Evalandgo. |
| [Update Unique Response](actions/update-unique-response.md) | PUT | Updates an existing unique response in Evalandgo. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Evalandgo. |
| [List Questionnaire Webhooks](actions/list-questionnaire-webhooks.md) | GET | Retrieves webhooks for a questionnaire from Evalandgo. |
| [Replace Webhook](actions/replace-webhook.md) | PUT | Updates an existing webhook in Evalandgo. |

