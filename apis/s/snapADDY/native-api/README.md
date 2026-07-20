# snapADDY: Native API Reference

A consolidated summary of snapADDY's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.snapaddy.com
- **OpenAPI specification:** https://developers.snapaddy.com/organization-rest-api/swagger.json
- **API base URL:** `https://api.snapaddy.com`

## Authentication

### API Token

Use your snapADDY API token. Runtime requests send the token in the x-api-token header.

### Credentials

- **API Key:** `apiKey` · required · Your snapADDY API token from the snapADDY system integration settings.

Send these headers with each API request:

```http
x-api-token: <apiKey>
```

[Official authentication documentation](https://developers.snapaddy.com/organization-rest-api/guides/getting-started)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact Item](actions/create-contact-item.md) | `POST /grabber/v1/contactitem` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/create-contact-item) |
| [Delete Contact Item](actions/delete-contact-item.md) | `DELETE /grabber/v1/contactitem/:itemId` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/delete-contact-item) |
| [Get Answer](actions/get-answer.md) | `GET /visitreport/v1/answer/:answerId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/answer) |
| [Get Answer Option](actions/get-answer-option.md) | `GET /visitreport/v1/answerOption/:answerOptionId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/answer-option) |
| [Get Contact Item](actions/get-contact-item.md) | `GET /grabber/v1/contactitem/:itemId` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-item) |
| [Get Contact Item Attachment](actions/get-contact-item-attachment.md) | `GET /grabber/v1/attachment/:contactItemId/:attachmentId` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-item-attachment) |
| [Get Contact List Count](actions/get-contact-list-count.md) | `GET /grabber/v1/contactlist/:listId/count` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-list-size) |
| [Get Current User](actions/get-current-user.md) | `GET /organization/v1/me` | [docs](https://developers.snapaddy.com/organization-rest-api/reference/current-user) |
| [Get Group](actions/get-group.md) | `GET /visitreport/v1/group/:groupId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/group) |
| [Get Participant](actions/get-participant.md) | `GET /visitreport/v1/participant/:participantId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/participant) |
| [Get Participant Attachment](actions/get-participant-attachment.md) | `GET /visitreport/v1/attachment/:questionnaireId/:participantId/:attachmentId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/participant-attachment) |
| [Get Question](actions/get-question.md) | `GET /visitreport/v1/question/:questionId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/question) |
| [Get Question Option](actions/get-question-option.md) | `GET /visitreport/v1/questionOption/:questionOptionId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/question-option) |
| [Get Questionnaire](actions/get-questionnaire.md) | `GET /visitreport/v1/backend/questionnaires/:questionnaireId` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/questionnaire) |
| [List Contact Items](actions/list-contact-items.md) | `GET /grabber/v1/contactlist/:listId/contactitems` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-items-from-contact-list) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /grabber/v1/contactlist` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/contact-lists) |
| [List Organization Users](actions/list-organization-users.md) | `GET /organization/v1/usernames` | [docs](https://developers.snapaddy.com/organization-rest-api/reference/organization-users) |
| [List Questionnaire Participants](actions/list-questionnaire-participants.md) | `GET /visitreport/v1/backend/questionnaires/:questionnaireId/participants/all` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/questionnaire-participants) |
| [List Questionnaires](actions/list-questionnaires.md) | `GET /visitreport/v1/backend/questionnaires/all` | [docs](https://developers.snapaddy.com/visitreport-rest-api/reference/questionnaires) |
| [Update Contact Item](actions/update-contact-item.md) | `PUT /grabber/v1/contactitem/:itemId` | [docs](https://developers.snapaddy.com/dataquality-rest-api/reference/update-contact-item) |
