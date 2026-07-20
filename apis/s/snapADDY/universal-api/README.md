# <img src="https://images.mindcloud.co/apps/icons/snapaddy-icon_1775839979204.png" alt="snapADDY logo" width="28" height="28"> snapADDY: Universal API

snapADDY APIs for organization users, contact lists and contact items, and VisitReport questionnaires, participants, answers, and attachments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snapADDY/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.snapaddy.com
- **Vendor API docs:** https://developers.snapaddy.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get Answer](actions/get-answer.md) | GET |  |

### Answer Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Answer Option](actions/get-answer-option.md) | GET |  |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Item Attachment](actions/get-contact-item-attachment.md) | GET |  |
| [Get Participant Attachment](actions/get-participant-attachment.md) | GET |  |

### Contact Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Item](actions/create-contact-item.md) | POST |  |
| [Delete Contact Item](actions/delete-contact-item.md) | DELETE |  |
| [Get Contact Item](actions/get-contact-item.md) | GET |  |
| [List Contact Items](actions/list-contact-items.md) | GET |  |
| [Update Contact Item](actions/update-contact-item.md) | PUT |  |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Lists](actions/list-contact-lists.md) | GET |  |

### Contact List Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact List Count](actions/get-contact-list-count.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [Get Participant](actions/get-participant.md) | GET |  |
| [List Questionnaire Participants](actions/list-questionnaire-participants.md) | GET |  |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Question](actions/get-question.md) | GET |  |

### Question Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Question Option](actions/get-question-option.md) | GET |  |

### Questionnaire

| Action | Method | Description |
| --- | --- | --- |
| [Get Questionnaire](actions/get-questionnaire.md) | GET |  |
| [List Questionnaires](actions/list-questionnaires.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Organization Users](actions/list-organization-users.md) | GET |  |

