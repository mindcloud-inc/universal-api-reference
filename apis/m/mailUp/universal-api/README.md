# <img src="https://images.mindcloud.co/apps/icons/mail-up_1773675397728.png" alt="MailUp logo" width="28" height="28"> MailUp: Universal API

Manage MailUp lists, subscribers, campaigns, sends, and delivery reporting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailUp/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailup.com/
- **Vendor API docs:** https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Get Authentication Details](actions/get-authentication-details.md) | GET | Retrieves authenticated user and console details from MailUp. |
| [Get Authentication Info](actions/get-authentication-info.md) | GET | Retrieves authenticated user and console info from MailUp. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | POST | Creates a new email message in MailUp. |
| [Get Email](actions/get-email.md) | GET | Retrieves an email message from MailUp. |
| [Get Email Send History](actions/get-email-send-history.md) | GET | Retrieves send history for a MailUp email. |
| [List Emails](actions/list-emails.md) | GET | Retrieves email messages from a MailUp list. |
| [Send Email](actions/send-email.md) | POST | Sends an email message to a MailUp list. |
| [Update Email](actions/update-email.md) | PUT | Updates an existing email message in MailUp. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in a MailUp list. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from a MailUp list. |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [Get Import](actions/get-import.md) | GET | Retrieves an import job from MailUp. |
| [List Imports](actions/list-imports.md) | GET | Retrieves existing import jobs from MailUp. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in MailUp. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from MailUp by list ID. |
| [List Lists](actions/list-lists.md) | GET | Retrieves existing mailing lists from MailUp. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in MailUp. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Import Recipient](actions/import-recipient.md) | POST | Imports a recipient into a MailUp list. |
| [Import Recipients](actions/import-recipients.md) | POST | Imports recipients into a MailUp list. |
| [List Pending Recipients](actions/list-pending-recipients.md) | GET | Retrieves pending recipients from a MailUp list. |
| [List Recipient Opt-ins](actions/list-recipient-opt-ins.md) | GET | Retrieves recipient opt-in details from a MailUp list. |
| [List Subscribed Recipients](actions/list-subscribed-recipients.md) | GET | Retrieves subscribed recipients from a MailUp list. |
| [List Unsubscribed Recipients](actions/list-unsubscribed-recipients.md) | GET | Retrieves unsubscribed recipients from a MailUp list. |
| [Subscribe Recipient](actions/subscribe-recipient.md) | PUT | Subscribes a recipient to a MailUp list. |
| [Unsubscribe Recipient](actions/unsubscribe-recipient.md) | DELETE | Unsubscribes a recipient from a MailUp list. |

