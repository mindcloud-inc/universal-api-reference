# <img src="https://images.mindcloud.co/apps/icons/blocksurvey-icon-square_1775847603196.png" alt="BlockSurvey logo" width="28" height="28"> BlockSurvey: Universal API

BlockSurvey is an end-to-end survey platform for creating secure surveys, managing audience contacts, and configuring response collection rules.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blockSurvey/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://blocksurvey.io
- **Vendor API docs:** https://documents.blocksurvey.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Survey Cut Off Date](actions/get-survey-cut-off-date.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-cut-off-date?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in BlockSurvey. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from BlockSurvey. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from BlockSurvey. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in BlockSurvey. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Cut Off Date](actions/get-survey-cut-off-date.md) | GET | Retrieves a survey cut off date from BlockSurvey. |
| [Get Survey Limit Maximum Response Count](actions/get-survey-limit-maximum-response-count.md) | GET | Retrieves a survey response limit from BlockSurvey. |
| [Get Survey Scheduled Start Date](actions/get-survey-scheduled-start-date.md) | GET | Retrieves a survey scheduled start date from BlockSurvey. |
| [Get Survey Text Variable Value](actions/get-survey-text-variable-value.md) | GET | Retrieves a survey text variable value from BlockSurvey. |
| [Update Survey Cut Off Date](actions/update-survey-cut-off-date.md) | PUT | Updates a survey cut off date in BlockSurvey. |
| [Update Survey Limit Maximum Response Count](actions/update-survey-limit-maximum-response-count.md) | PUT | Updates a survey response limit in BlockSurvey. |
| [Update Survey Scheduled Start Date](actions/update-survey-scheduled-start-date.md) | PUT | Updates a survey scheduled start date in BlockSurvey. |
| [Update Survey Text Variable Value](actions/update-survey-text-variable-value.md) | PUT | Updates a survey text variable value in BlockSurvey. |

