# <img src="https://images.mindcloud.co/apps/icons/blip-icon_1775483567814.png" alt="Blip logo" width="28" height="28"> Blip: Universal API

BLiP is a conversational platform for building, operating, and analyzing bots, tickets, contacts, threads, and related messaging workflows over the BLiP command API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blip/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blip.ai/
- **Vendor API docs:** https://docs.blip.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blip/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Blip. |
| [Ping](actions/ping.md) | GET | Retrieves a ping response from Blip. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in Blip. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Blip. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Blip. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Blip. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Last Messages](actions/list-last-messages.md) | GET | Retrieves recent messages from Blip. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Blip. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Blip. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Blip. |
| [Store Custom Document](actions/store-custom-document.md) | POST | Creates a custom document in Blip. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [List Attendants](actions/list-attendants.md) | GET | Retrieves attendants from Blip. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create Distribution List](actions/create-distribution-list.md) | POST | Creates a distribution list in Blip. |
| [Delete Distribution List](actions/delete-distribution-list.md) | DELETE | Deletes a distribution list from Blip. |
| [List Distribution Lists](actions/list-distribution-lists.md) | GET | Retrieves distribution lists from Blip. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Logged Messages](actions/list-logged-messages.md) | GET | Retrieves logged messages from Blip. |
| [Toggle Message and Notification Logs](actions/toggle-message-and-notification-logs.md) | PUT | Updates message and notification log settings in Blip. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Associate Answer to Intent](actions/associate-answer-to-intent.md) | POST | Associates an answer with an intent in Blip. |
| [Associate Question to Intent](actions/associate-question-to-intent.md) | POST | Associates a question with an intent in Blip. |
| [Create Entity](actions/create-entity.md) | POST | Creates an entity in Blip. |
| [Create Intent](actions/create-intent.md) | POST | Creates an intent in Blip. |
| [Delete Answer from Intent](actions/delete-answer-from-intent.md) | DELETE | Deletes an answer from an intent in Blip. |
| [Delete Question from Intent](actions/delete-question-from-intent.md) | DELETE | Deletes a question from an intent in Blip. |
| [Get Entity](actions/get-entity.md) | GET | Retrieves an entity from Blip. |
| [Get Intent](actions/get-intent.md) | GET | Retrieves an intent from Blip. |
| [List Entities](actions/list-entities.md) | GET | Retrieves entities from Blip. |
| [List Intent Answers](actions/list-intent-answers.md) | GET | Retrieves answers for an intent in Blip. |
| [List Intent Questions](actions/list-intent-questions.md) | GET | Retrieves questions for an intent in Blip. |
| [List Intents](actions/list-intents.md) | GET | Retrieves intents from Blip. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Dashboard Detail](actions/get-call-dashboard-detail.md) | GET | Retrieves call dashboard details from Blip. |
| [Get Call Dashboard Summary](actions/get-call-dashboard-summary.md) | GET | Retrieves a call dashboard summary from Blip. |
| [Get Call Reject Reasons](actions/get-call-reject-reasons.md) | GET | Retrieves call reject reasons from Blip. |
| [List Analysis](actions/list-analysis.md) | GET | Retrieves recent analysis from Blip. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduling](actions/cancel-scheduling.md) | DELETE | Cancels a scheduling in Blip. |
| [Create Scheduling](actions/create-scheduling.md) | POST | Creates a message scheduling in Blip. |
| [Get Scheduled Message](actions/get-scheduled-message.md) | GET | Retrieves a scheduled message from Blip. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Blip. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Closed Tickets](actions/list-closed-tickets.md) | GET | Retrieves closed tickets from Blip. |
| [List Open Tickets](actions/list-open-tickets.md) | GET | Retrieves open tickets from Blip. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Blip. |

