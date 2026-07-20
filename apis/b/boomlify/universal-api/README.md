# <img src="https://images.mindcloud.co/apps/icons/boomlify_1780952365110.png" alt="Boomlify logo" width="28" height="28"> Boomlify: Universal API

Boomlify provides temporary email inboxes and API access for creating disposable email addresses, reading messages, managing dashboard inboxes, and checking account usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boomlify/latest
- **Category:** Communication / Email Communications
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://boomlify.com/
- **Vendor API docs:** https://boomlify.com/en/temp-mail-api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Credits](actions/get-account-credits.md) | GET | Retrieves credit balance and usage information from Boomlify. |

### Account Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account information from Boomlify. |

### Account Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves API usage statistics from Boomlify. |

### Dashboard Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Dashboard Email](actions/create-dashboard-email.md) | POST | Creates a new dashboard email in Boomlify. |
| [Get Dashboard Email](actions/get-dashboard-email.md) | GET | Retrieves details for a dashboard email from Boomlify. |
| [List Dashboard Emails](actions/list-dashboard-emails.md) | GET | Retrieves dashboard-created and API emails from Boomlify. |

### Dashboard Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Email Messages](actions/get-dashboard-email-messages.md) | GET | Retrieves received messages for a dashboard email in Boomlify. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | POST | Creates a new temporary email address in Boomlify. |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an existing email from Boomlify. |
| [Get Email](actions/get-email.md) | GET | Retrieves details for a temporary email from Boomlify. |
| [List Emails](actions/list-emails.md) | GET | Retrieves active temporary emails from Boomlify. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Messages](actions/get-email-messages.md) | GET | Retrieves messages for a temporary email in Boomlify. |

### Telegram Forwarding

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Enable Dashboard Telegram Forwarding](actions/bulk-enable-dashboard-telegram-forwarding.md) | PUT | Bulk enables Telegram forwarding for owned mailboxes in Boomlify. |
| [Get Dashboard Telegram Forwarding](actions/get-dashboard-telegram-forwarding.md) | GET | Retrieves Telegram forwarding status for an owned mailbox in Boomlify. |
| [Update Dashboard Telegram Forwarding](actions/update-dashboard-telegram-forwarding.md) | PUT | Updates Telegram forwarding for an owned mailbox in Boomlify. |

