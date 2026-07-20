# <img src="https://images.mindcloud.co/apps/icons/webex-interact-icon_1776787928769.png" alt="Webex Interact logo" width="28" height="28"> Webex Interact: Universal API

Send SMS messages, manage contacts and lists, create short links, inspect account metadata, and manage scheduled SMS requests with Webex Interact.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webexInteract/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webexinteract.com/
- **Vendor API docs:** https://docs.webexinteract.com/reference/webex-interact-api-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve account metadata](actions/retrieve-account-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/retrieve-account-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve account metadata](actions/retrieve-account-metadata.md) | GET | Retrieves account metadata from Webex Interact. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create or update contacts](actions/create-or-update-contacts.md) | POST | Creates or updates contacts in Webex Interact. |
| [Delete contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Webex Interact. |
| [List contacts in list](actions/list-contacts-in-list.md) | GET | Retrieves contacts from a list in Webex Interact. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create contact list](actions/create-contact-list.md) | POST | Creates a new contact list in Webex Interact. |
| [Delete contact list](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from Webex Interact. |
| [List contact lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Webex Interact. |

### Scheduled Sms Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel scheduled SMS request](actions/cancel-scheduled-sms-request.md) | DELETE | Cancels a scheduled SMS request in Webex Interact. |
| [List scheduled SMS by created date range](actions/list-scheduled-sms-by-created-date-range.md) | GET | Finds scheduled SMS requests in Webex Interact by created date range. |
| [List scheduled SMS by scheduled date range](actions/list-scheduled-sms-by-scheduled-date-range.md) | GET | Finds scheduled SMS requests in Webex Interact by scheduled date range. |
| [Retrieve scheduled SMS request](actions/retrieve-scheduled-sms-request.md) | GET | Finds a scheduled SMS request in Webex Interact by ID. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Delete sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from Webex Interact. |
| [List senders](actions/list-senders.md) | GET | Retrieves senders from Webex Interact. |
| [Retrieve sender](actions/retrieve-sender.md) | GET | Retrieves a sender from Webex Interact. |

### Shortlink

| Action | Method | Description |
| --- | --- | --- |
| [Create shortlink](actions/create-shortlink.md) | POST | Creates a new shortlink in Webex Interact. |
| [Delete shortlink](actions/delete-shortlink.md) | DELETE | Deletes an existing shortlink from Webex Interact. |
| [Filter shortlinks](actions/filter-shortlinks.md) | GET | Finds shortlinks in Webex Interact by filter criteria. |
| [Retrieve shortlink](actions/retrieve-shortlink.md) | GET | Retrieves a shortlink from Webex Interact. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send template SMS](actions/send-template-sms.md) | POST | Sends a template SMS from Webex Interact. |
| [Send text SMS](actions/send-text-sms.md) | POST | Sends an SMS message from Webex Interact. |
| [Test template SMS](actions/test-template-sms.md) | POST | Tests a template SMS in Webex Interact. |

### Sms Test

| Action | Method | Description |
| --- | --- | --- |
| [Test text SMS](actions/test-text-sms.md) | POST | Tests an SMS message in Webex Interact. |

