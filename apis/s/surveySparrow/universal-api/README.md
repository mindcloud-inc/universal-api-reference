# <img src="https://images.mindcloud.co/apps/icons/unnamed-9_1774636179187.png" alt="SurveySparrow logo" width="28" height="28"> SurveySparrow: Universal API

Create, send, and analyze surveys, manage contacts, and automate feedback workflows in SurveySparrow.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/surveySparrow/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://surveysparrow.com/
- **Vendor API docs:** https://developers.surveysparrow.com/rest-apis/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Translation](actions/export-translation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/export-translation?connectionId=$CONNECTION_ID&surveyId=1&languageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Log](actions/get-audit-log.md) | GET | Retrieves an audit log from SurveySparrow. |
| [List Audit Logs](actions/list-audit-logs.md) | GET | Retrieves audit logs from SurveySparrow. |

### Audit Log Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Audit Log Event](actions/create-audit-log-event.md) | POST | Creates a subscribed audit log event in SurveySparrow. |
| [Delete Audit Log Event](actions/delete-audit-log-event.md) | DELETE | Deletes a subscribed audit log event from SurveySparrow. |
| [List Audit Log Events](actions/list-audit-log-events.md) | GET | Retrieves subscribed audit log events from SurveySparrow. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from SurveySparrow. |
| [List Channels](actions/list-channels.md) | GET | Retrieves all channels from SurveySparrow. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in SurveySparrow. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from SurveySparrow. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from SurveySparrow. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contacts from SurveySparrow. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in SurveySparrow. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in SurveySparrow. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from SurveySparrow. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from SurveySparrow. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves all contact lists from SurveySparrow. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in SurveySparrow. |

### Contact Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Property](actions/create-contact-property.md) | POST | Creates a new contact property in SurveySparrow. |
| [Delete Contact Property](actions/delete-contact-property.md) | DELETE | Deletes an existing contact property from SurveySparrow. |
| [List Contact Properties](actions/list-contact-properties.md) | GET | Retrieves all contact properties from SurveySparrow. |
| [Update Contact Property](actions/update-contact-property.md) | PUT | Updates an existing contact property in SurveySparrow. |

### Expression

| Action | Method | Description |
| --- | --- | --- |
| [List Expressions](actions/list-expressions.md) | GET | Retrieves survey expressions from SurveySparrow. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Create Language](actions/create-language.md) | POST | Creates a custom language in SurveySparrow. |
| [List Languages](actions/list-languages.md) | GET | Retrieves translation languages from SurveySparrow. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | GET | Retrieves survey questions from SurveySparrow. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET | Retrieves all responses from SurveySparrow. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves all roles from SurveySparrow. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET | Retrieves a survey from SurveySparrow. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves all surveys from SurveySparrow. |

### Survey Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Folder](actions/create-survey-folder.md) | POST | Creates a new survey folder in SurveySparrow. |
| [Delete Survey Folder](actions/delete-survey-folder.md) | DELETE | Deletes an existing survey folder from SurveySparrow. |
| [Get Survey Folder](actions/get-survey-folder.md) | GET | Retrieves a survey folder from SurveySparrow. |
| [List Survey Folders](actions/list-survey-folders.md) | GET | Retrieves all survey folders from SurveySparrow. |
| [Update Survey Folder](actions/update-survey-folder.md) | PUT | Updates an existing survey folder in SurveySparrow. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves all teams from SurveySparrow. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Export Translation](actions/export-translation.md) | GET | Retrieves a translation Excel file from SurveySparrow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from SurveySparrow. |
| [List Users](actions/list-users.md) | GET | Retrieves all users from SurveySparrow. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Variables](actions/create-survey-variables.md) | POST | Creates survey variables in SurveySparrow. |
| [Create Variable](actions/create-variable.md) | POST | Creates a survey variable in SurveySparrow. |
| [Delete Variable](actions/delete-variable.md) | DELETE | Deletes a survey variable from SurveySparrow. |
| [List Variables](actions/list-variables.md) | GET | Retrieves survey variables from SurveySparrow. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in SurveySparrow. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from SurveySparrow. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhooks from SurveySparrow. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in SurveySparrow. |

