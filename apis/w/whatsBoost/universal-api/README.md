# <img src="https://images.mindcloud.co/apps/icons/whats-boost_1776272333750.png" alt="WhatsBoost logo" width="28" height="28"> WhatsBoost: Universal API

WhatsBoost lets you send SMS, WhatsApp, OTP, and USSD requests and manage related campaigns, contacts, devices, and account resources through the WhatsBoost REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whatsBoost/latest
- **Category:** Communication / Team Messaging
- **Actions:** 54
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whatsboost.net
- **Vendor API docs:** https://whatsboost.net/developer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Devices](actions/get-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/get-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (54)

### Bulk Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST | Sends bulk SMS messages from WhatsBoost. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Delete SMS Campaign](actions/delete-sms-campaign.md) | DELETE | Deletes an SMS campaign from WhatsBoost. |
| [Delete WhatsApp Campaign](actions/delete-whats-app-campaign.md) | DELETE | Deletes a WhatsApp campaign from WhatsBoost. |
| [Get SMS Campaigns](actions/get-sms-campaigns.md) | GET | Retrieves SMS campaigns from WhatsBoost. |
| [Get WhatsApp Campaigns](actions/get-whats-app-campaigns.md) | GET | Retrieves WhatsApp campaigns from WhatsBoost. |
| [Start SMS Campaign](actions/start-sms-campaign.md) | PUT | Starts an SMS campaign in WhatsBoost. |
| [Start WhatsApp Campaign](actions/start-whats-app-campaign.md) | PUT | Starts a WhatsApp campaign in WhatsBoost. |
| [Stop SMS Campaign](actions/stop-sms-campaign.md) | PUT | Stops an SMS campaign in WhatsBoost. |
| [Stop WhatsApp Campaign](actions/stop-whats-app-campaign.md) | PUT | Stops a WhatsApp campaign in WhatsBoost. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in WhatsBoost. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from WhatsBoost. |
| [Get Contacts](actions/get-contacts.md) | GET | Retrieves contacts from WhatsBoost. |
| [Get WhatsApp Group Contacts](actions/get-whats-app-group-contacts.md) | GET | Retrieves WhatsApp group contacts from WhatsBoost. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Devices](actions/get-devices.md) | GET | Retrieves devices from WhatsBoost. |

### Gateway Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Gateway Rates](actions/get-gateway-rates.md) | GET | Retrieves gateway rates from WhatsBoost. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in WhatsBoost. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from WhatsBoost. |
| [Get Groups](actions/get-groups.md) | GET | Retrieves groups from WhatsBoost. |
| [Get WhatsApp Groups](actions/get-whats-app-groups.md) | GET | Retrieves WhatsApp groups from WhatsBoost. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Received Chat](actions/delete-received-chat.md) | DELETE | Deletes a received chat from WhatsBoost. |
| [Delete Received Message](actions/delete-received-message.md) | DELETE | Deletes a received message from WhatsBoost. |
| [Delete Sent Chat](actions/delete-sent-chat.md) | DELETE | Deletes a sent chat from WhatsBoost. |
| [Delete Sent Message](actions/delete-sent-message.md) | DELETE | Deletes a sent message from WhatsBoost. |
| [Get Pending Chats](actions/get-pending-chats.md) | GET | Retrieves pending chats from WhatsBoost. |
| [Get Pending Messages](actions/get-pending-messages.md) | GET | Retrieves pending messages from WhatsBoost. |
| [Get Received Chats](actions/get-received-chats.md) | GET | Retrieves received chats from WhatsBoost. |
| [Get Received Messages](actions/get-received-messages.md) | GET | Retrieves received messages from WhatsBoost. |
| [Get Sent Chats](actions/get-sent-chats.md) | GET | Retrieves sent chats from WhatsBoost. |
| [Get Sent Messages](actions/get-sent-messages.md) | GET | Retrieves sent messages from WhatsBoost. |
| [Get Single Chat](actions/get-single-chat.md) | GET | Retrieves a chat by ID from WhatsBoost. |
| [Get Single Message](actions/get-single-message.md) | GET | Retrieves a message by ID from WhatsBoost. |
| [Send Bulk Chats](actions/send-bulk-chats.md) | POST | Sends bulk chat messages from WhatsBoost. |
| [Send Single Chat](actions/send-single-chat.md) | POST | Sends a single chat message from WhatsBoost. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Delete Android Notification](actions/delete-android-notification.md) | DELETE | Deletes an Android notification from WhatsBoost. |

### Otp Request

| Action | Method | Description |
| --- | --- | --- |
| [Send OTP](actions/send-otp.md) | POST | Sends a one-time password from WhatsBoost. |

### Otp Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify OTP](actions/verify-otp.md) | GET | Verifies a one-time password in WhatsBoost. |

### Partner Earning

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Earnings](actions/get-partner-earnings.md) | GET | Retrieves partner earnings from WhatsBoost. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Validate a WhatsApp phone number](actions/validate-a-whats-app-phone-number.md) | GET | Validates a WhatsApp phone number in WhatsBoost. |

### Shortener

| Action | Method | Description |
| --- | --- | --- |
| [Get Shorteners](actions/get-shorteners.md) | GET | Retrieves shorteners from WhatsBoost. |

### Single Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send Single SMS](actions/send-single-sms.md) | POST | Sends a single SMS from WhatsBoost. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Package](actions/get-subscription-package.md) | GET | Retrieves the subscription package from WhatsBoost. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET | Retrieves remaining credits from WhatsBoost. |

### Unsubscribed Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Unsubscribed](actions/delete-unsubscribed.md) | DELETE | Deletes an unsubscribed contact from WhatsBoost. |
| [Get Unsubscribed](actions/get-unsubscribed.md) | GET | Retrieves unsubscribed contacts from WhatsBoost. |

### Ussd Request

| Action | Method | Description |
| --- | --- | --- |
| [Delete USSD Request](actions/delete-ussd-request.md) | DELETE | Deletes a USSD request from WhatsBoost. |
| [Get USSD Requests](actions/get-ussd-requests.md) | GET | Retrieves USSD requests from WhatsBoost. |
| [Send USSD Request](actions/send-ussd-request.md) | POST | Sends a USSD request from WhatsBoost. |

### Whatsapp Account

| Action | Method | Description |
| --- | --- | --- |
| [Delete WhatsApp Account](actions/delete-whats-app-account.md) | DELETE | Deletes a WhatsApp account from WhatsBoost. |
| [Get Accounts](actions/get-accounts.md) | GET | Retrieves WhatsApp accounts from WhatsBoost. |
| [Get WhatsApp information after linking](actions/get-whats-app-information-after-linking.md) | GET | Retrieves WhatsApp account info after linking in WhatsBoost. |
| [Link WhatsApp Account](actions/link-whats-app-account.md) | POST | Links a WhatsApp account in WhatsBoost. |
| [Relink WhatsApp Account](actions/relink-whats-app-account.md) | POST | Relinks a WhatsApp account in WhatsBoost. |

### Whatsapp Qr

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp QR Image](actions/get-whats-app-qr-image.md) | GET | Retrieves a WhatsApp QR image from WhatsBoost. |

### Whatsapp Server

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp Servers](actions/get-whats-app-servers.md) | GET | Retrieves WhatsApp servers from WhatsBoost. |

