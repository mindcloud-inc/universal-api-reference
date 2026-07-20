# <img src="https://images.mindcloud.co/apps/icons/get-salesio_1776778230230.png" alt="GetSales.io logo" width="28" height="28"> GetSales.io: Universal API

GetSales.io is a sales engagement platform for managing contacts, lists, automations, sender profiles, and inbox messaging through its public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/getSalesio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getsales.io
- **Vendor API docs:** https://api.getsales.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Automation](actions/add-contact-to-automation.md) | PUT |  |
| [Cancel Contact From All Automations](actions/cancel-contact-from-all-automations.md) | PUT |  |
| [Cancel Contact From Automations](actions/cancel-contact-from-automations.md) | PUT |  |
| [List Automations](actions/list-automations.md) | GET |  |
| [Start Automation](actions/start-automation.md) | PUT |  |
| [Stop Automation](actions/stop-automation.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add New Contact To Automation](actions/add-new-contact-to-automation.md) | POST |  |
| [Create Contacts](actions/create-contacts.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Find Contact](actions/find-contact.md) | GET |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/search-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |
| [Create Or Update Contact](actions/upsert-contact.md) | POST |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List Emails](actions/list-emails.md) | GET |  |
| [Send Email](actions/send-email.md) | POST |  |

### Linkedin Message

| Action | Method | Description |
| --- | --- | --- |
| [List LinkedIn Messages](actions/list-linked-in-messages.md) | GET |  |
| [Send LinkedIn Message](actions/send-linked-in-message.md) | POST |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Get List](actions/get-list.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |

### Sender Profile

| Action | Method | Description |
| --- | --- | --- |
| [Connect Sender Profile With GoLogin](actions/connect-sender-profile-with-go-login.md) | PUT |  |
| [Create Sender Profile](actions/create-sender-profile.md) | POST |  |
| [Get Sender Profile](actions/get-sender-profile.md) | GET |  |
| [List Sender Profiles](actions/list-sender-profiles.md) | GET |  |

