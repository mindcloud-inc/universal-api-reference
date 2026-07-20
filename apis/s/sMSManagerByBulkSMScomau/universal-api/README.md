# <img src="https://images.mindcloud.co/apps/icons/sms-manager-by-bulk-sms_1782741120814.png" alt="SMS Manager by BulkSMS.com.au logo" width="28" height="28"> SMS Manager by BulkSMS.com.au: Universal API

SMS Manager by BulkSMS.com.au provides a REST API for validating API keys, checking account context, managing SMS account resources, and sending SMS through the SMS Manager v2 platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSManagerByBulkSMScomau/latest
- **Category:** Marketing
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smsmanager.com.au/
- **Vendor API docs:** https://smsmanager.com.au/v2/api_docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSManagerByBulkSMScomau/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Accessible Accounts](actions/list-accessible-accounts.md) | GET |  |
| [List Shared Accounts](actions/list-shared-accounts.md) | GET |  |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET |  |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Configuration](actions/get-client-configuration.md) | GET |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Settings](actions/get-account-settings.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Export Contacts](actions/export-contacts.md) | GET |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Get Message Recipients](actions/get-message-recipients.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Group Contacts](actions/list-group-contacts.md) | GET |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Conversations](actions/list-chat-conversations.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Contact Fields](actions/list-custom-contact-fields.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Automation Event Data](actions/get-sample-automation-event-data.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Get My Pending Invitations](actions/get-my-pending-invitations.md) | GET |  |
| [List Pending Invitations](actions/list-pending-invitations.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [View Invoice](actions/view-invoice.md) | GET |  |

### Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword](actions/get-keyword.md) | GET |  |
| [List Keywords](actions/list-keywords.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Export Message History](actions/export-message-history.md) | GET |  |
| [Get Chat Message History](actions/get-chat-message-history.md) | GET |  |
| [Get Message](actions/get-message.md) | GET |  |
| [Get Message Details](actions/get-message-details.md) | GET |  |
| [Get Message History](actions/get-message-history.md) | GET |  |
| [Get Message Replies](actions/get-message-replies.md) | GET |  |
| [List Incoming Messages](actions/list-incoming-messages.md) | GET |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Details](actions/get-payment-details.md) | GET |  |
| [Get Stored Payment Cards](actions/get-stored-payment-cards.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Auto Top-Up Settings](actions/get-auto-top-up-settings.md) | GET |  |
| [List Credit Purchase History](actions/list-credit-purchase-history.md) | GET |  |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Permissions](actions/get-available-permissions.md) | GET |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Get Blocked Number](actions/get-blocked-number.md) | GET |  |
| [List Blocked Numbers](actions/list-blocked-numbers.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Statistics](actions/get-message-statistics.md) | GET |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Packages](actions/list-credit-packages.md) | GET |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Subscription](actions/get-automation-subscription.md) | GET |  |
| [List Automation Subscriptions](actions/list-automation-subscriptions.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET |  |

