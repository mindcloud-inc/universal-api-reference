# <img src="https://images.mindcloud.co/apps/icons/click-send_1772727340356.png" alt="ClickSend SMS logo" width="28" height="28"> ClickSend SMS: Universal API

ClickSend SMS is a messaging API for sending, receiving, and managing global SMS workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clickSendSMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clicksend.com
- **Vendor API docs:** https://developers.clicksend.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Calculate SMS Campaign Price](actions/calculate-sms-campaign-price.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-campaign-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Alpha Tag

| Action | Method | Description |
| --- | --- | --- |
| [Request Alpha Tag](actions/request-alpha-tag.md) | POST | Requests a new alpha tag in ClickSend SMS. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in a ClickSend SMS list. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a ClickSend SMS list. |

### Contact Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into a ClickSend SMS list. |

### Inbound Sms

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbound SMS](actions/get-inbound-sms.md) | GET | Retrieves an inbound SMS message from ClickSend SMS. |
| [List Inbound SMS](actions/list-inbound-sms.md) | GET | Retrieves inbound SMS messages from ClickSend SMS. |
| [Mark Inbound SMS as Read](actions/mark-inbound-sms-as-read.md) | PUT | Marks inbound SMS messages as read in ClickSend SMS. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new contact list in ClickSend SMS. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from ClickSend SMS. |

### Number

| Action | Method | Description |
| --- | --- | --- |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves dedicated numbers from ClickSend SMS. |

### Sms Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Cancel SMS Campaign](actions/cancel-sms-campaign.md) | PUT | Cancels an existing SMS campaign in ClickSend SMS. |
| [Get SMS Campaign](actions/get-sms-campaign.md) | GET | Retrieves an SMS campaign from ClickSend SMS. |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET | Retrieves SMS campaigns from ClickSend SMS. |
| [Send SMS Campaign](actions/send-sms-campaign.md) | POST | Creates and sends an SMS campaign in ClickSend SMS. |
| [Update SMS Campaign](actions/update-sms-campaign.md) | PUT | Updates an existing SMS campaign in ClickSend SMS. |

### Sms Campaign Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate SMS Campaign Price](actions/calculate-sms-campaign-price.md) | GET | Calculates SMS campaign pricing in ClickSend SMS. |

### Sms History

| Action | Method | Description |
| --- | --- | --- |
| [List SMS History](actions/list-sms-history.md) | GET | Retrieves SMS history from ClickSend SMS. |

### Sms History Export

| Action | Method | Description |
| --- | --- | --- |
| [Export SMS History](actions/export-sms-history.md) | GET | Exports SMS history from ClickSend SMS. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Cancel SMS](actions/cancel-sms.md) | PUT | Cancels an SMS message in ClickSend SMS. |
| [Send SMS](actions/send-sms.md) | POST | Creates a new SMS message in ClickSend SMS. |

### Sms Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate SMS Price](actions/calculate-sms-price.md) | GET | Calculates SMS pricing in ClickSend SMS. |

### Sms Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Receipt](actions/get-sms-receipt.md) | GET | Retrieves an SMS receipt from ClickSend SMS. |
| [List SMS Receipts](actions/list-sms-receipts.md) | GET | Retrieves SMS receipts from ClickSend SMS. |
| [Mark SMS Receipt As Read](actions/mark-sms-receipt-as-read.md) | PUT | Marks SMS receipts as read in ClickSend SMS. |

### Sms Template

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Template](actions/create-sms-template.md) | POST | Creates a new SMS template in ClickSend SMS. |
| [Delete SMS Template](actions/delete-sms-template.md) | DELETE | Deletes an existing SMS template from ClickSend SMS. |
| [Get SMS Template](actions/get-sms-template.md) | GET | Retrieves an SMS template from ClickSend SMS. |
| [List SMS Templates](actions/list-sms-templates.md) | GET | Retrieves SMS templates from ClickSend SMS. |
| [Update SMS Template](actions/update-sms-template.md) | PUT | Updates an existing SMS template in ClickSend SMS. |

