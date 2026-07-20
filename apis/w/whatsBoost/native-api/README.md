# WhatsBoost: Native API Reference

A consolidated summary of WhatsBoost's API configuration and 54 documented operations, with links to official documentation.

- **Official docs:** https://whatsboost.net/developer
- **API base URL:** `https://whatsboost.net/api`

## Authentication

### API Key

Custom auth for WhatsBoost API keys sent as the POST body field secret.

### Credentials

- **API Key:** `apiKey` · required · Your WhatsBoost API key. WhatsBoost requires it as the POST body field `secret` on every request.

[Official authentication documentation](https://whatsboost.net/developer/autenticacion)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (54 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /create/contact` | [docs](https://whatsboost.net/api) |
| [Create Group](actions/create-group.md) | `POST /create/group` | [docs](https://whatsboost.net/api) |
| [Delete Android Notification](actions/delete-android-notification.md) | `POST /delete/notification` | [docs](https://whatsboost.net/api) |
| [Delete Contact](actions/delete-contact.md) | `POST /delete/contact` | [docs](https://whatsboost.net/api) |
| [Delete Group](actions/delete-group.md) | `POST /delete/group` | [docs](https://whatsboost.net/api) |
| [Delete Received Chat](actions/delete-received-chat.md) | `POST /delete/wa.received` | [docs](https://whatsboost.net/api) |
| [Delete Received Message](actions/delete-received-message.md) | `POST /delete/sms.received` | [docs](https://whatsboost.net/api) |
| [Delete Sent Chat](actions/delete-sent-chat.md) | `POST /delete/wa.sent` | [docs](https://whatsboost.net/api) |
| [Delete Sent Message](actions/delete-sent-message.md) | `POST /delete/sms.sent` | [docs](https://whatsboost.net/api) |
| [Delete SMS Campaign](actions/delete-sms-campaign.md) | `POST /delete/sms.campaign` | [docs](https://whatsboost.net/api) |
| [Delete Unsubscribed](actions/delete-unsubscribed.md) | `POST /delete/unsubscribed` | [docs](https://whatsboost.net/api) |
| [Delete USSD Request](actions/delete-ussd-request.md) | `POST /delete/ussd` | [docs](https://whatsboost.net/api) |
| [Delete WhatsApp Account](actions/delete-whats-app-account.md) | `POST /delete/wa.account` | [docs](https://whatsboost.net/api) |
| [Delete WhatsApp Campaign](actions/delete-whats-app-campaign.md) | `POST /delete/wa.campaign` | [docs](https://whatsboost.net/api) |
| [Get Accounts](actions/get-accounts.md) | `POST /get/wa.accounts` | [docs](https://whatsboost.net/api) |
| [Get Contacts](actions/get-contacts.md) | `POST /get/contacts` | [docs](https://whatsboost.net/api) |
| [Get Devices](actions/get-devices.md) | `POST /get/devices` | [docs](https://whatsboost.net/api) |
| [Get Gateway Rates](actions/get-gateway-rates.md) | `POST /get/rates` | [docs](https://whatsboost.net/api) |
| [Get Groups](actions/get-groups.md) | `POST /get/groups` | [docs](https://whatsboost.net/api) |
| [Get Partner Earnings](actions/get-partner-earnings.md) | `POST /get/earnings` | [docs](https://whatsboost.net/api) |
| [Get Pending Chats](actions/get-pending-chats.md) | `POST /get/wa.pending` | [docs](https://whatsboost.net/api) |
| [Get Pending Messages](actions/get-pending-messages.md) | `POST /get/sms.pending` | [docs](https://whatsboost.net/api) |
| [Get Received Chats](actions/get-received-chats.md) | `POST /get/wa.received` | [docs](https://whatsboost.net/api) |
| [Get Received Messages](actions/get-received-messages.md) | `POST /get/sms.received` | [docs](https://whatsboost.net/api) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `POST /get/credits` | [docs](https://whatsboost.net/api) |
| [Get Sent Chats](actions/get-sent-chats.md) | `POST /get/wa.sent` | [docs](https://whatsboost.net/api) |
| [Get Sent Messages](actions/get-sent-messages.md) | `POST /get/sms.sent` | [docs](https://whatsboost.net/api) |
| [Get Shorteners](actions/get-shorteners.md) | `POST /get/shorteners` | [docs](https://whatsboost.net/api) |
| [Get Single Chat](actions/get-single-chat.md) | `POST /get/wa.message` | [docs](https://whatsboost.net/api) |
| [Get Single Message](actions/get-single-message.md) | `POST /get/sms.message` | [docs](https://whatsboost.net/api) |
| [Get SMS Campaigns](actions/get-sms-campaigns.md) | `POST /get/sms.campaigns` | [docs](https://whatsboost.net/api) |
| [Get Subscription Package](actions/get-subscription-package.md) | `POST /get/subscription` | [docs](https://whatsboost.net/api) |
| [Get Unsubscribed](actions/get-unsubscribed.md) | `POST /get/unsubscribed` | [docs](https://whatsboost.net/api) |
| [Get USSD Requests](actions/get-ussd-requests.md) | `POST /get/ussd` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp Campaigns](actions/get-whats-app-campaigns.md) | `POST /get/wa.campaigns` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp Group Contacts](actions/get-whats-app-group-contacts.md) | `POST /get/wa.group.contacts` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp Groups](actions/get-whats-app-groups.md) | `POST /get/wa.groups` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp information after linking](actions/get-whats-app-information-after-linking.md) | `POST /get/wa.info` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp QR Image](actions/get-whats-app-qr-image.md) | `POST /get/wa.qr` | [docs](https://whatsboost.net/api) |
| [Get WhatsApp Servers](actions/get-whats-app-servers.md) | `POST /get/wa.servers` | [docs](https://whatsboost.net/api) |
| [Link WhatsApp Account](actions/link-whats-app-account.md) | `POST /create/wa.link` | [docs](https://whatsboost.net/api) |
| [Relink WhatsApp Account](actions/relink-whats-app-account.md) | `POST /create/wa.relink` | [docs](https://whatsboost.net/api) |
| [Send Bulk Chats](actions/send-bulk-chats.md) | `POST /send/whatsapp.bulk` | [docs](https://whatsboost.net/api) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /send/sms.bulk` | [docs](https://whatsboost.net/api) |
| [Send OTP](actions/send-otp.md) | `POST /send/otp` | [docs](https://whatsboost.net/api) |
| [Send Single Chat](actions/send-single-chat.md) | `POST /send/whatsapp` | [docs](https://whatsboost.net/api) |
| [Send Single SMS](actions/send-single-sms.md) | `POST /send/sms` | [docs](https://whatsboost.net/api) |
| [Send USSD Request](actions/send-ussd-request.md) | `POST /send/ussd` | [docs](https://whatsboost.net/api) |
| [Start SMS Campaign](actions/start-sms-campaign.md) | `POST /remote/start.sms` | [docs](https://whatsboost.net/api) |
| [Start WhatsApp Campaign](actions/start-whats-app-campaign.md) | `POST /remote/start.chats` | [docs](https://whatsboost.net/api) |
| [Stop SMS Campaign](actions/stop-sms-campaign.md) | `POST /remote/stop.sms` | [docs](https://whatsboost.net/api) |
| [Stop WhatsApp Campaign](actions/stop-whats-app-campaign.md) | `POST /remote/stop.chats` | [docs](https://whatsboost.net/api) |
| [Validate a WhatsApp phone number](actions/validate-a-whats-app-phone-number.md) | `POST /validate/whatsapp` | [docs](https://whatsboost.net/api) |
| [Verify OTP](actions/verify-otp.md) | `POST /get/otp` | [docs](https://whatsboost.net/api) |
