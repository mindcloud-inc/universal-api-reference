# <img src="https://images.mindcloud.co/apps/icons/37155205_1774031034134.png" alt="Seven logo" width="28" height="28"> Seven: Universal API

Send and manage SMS, voice calls, number lookups, contacts, numbers, subaccounts, and webhooks with seven.io.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seven/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seven.io
- **Vendor API docs:** https://docs.seven.io/en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Available Number

| Action | Method | Description |
| --- | --- | --- |
| [List Available Numbers](actions/list-available-numbers.md) | GET | Retrieves available numbers from Seven. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves current account balance from Seven. |

### Cnam Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get CNAM Lookup](actions/get-cnam-lookup.md) | GET | Retrieves CNAM lookup details from Seven. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Seven. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Seven. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Seven. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Seven. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Seven. |

### Credit Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Credits to Subaccount](actions/transfer-credits-to-subaccount.md) | POST | Creates a subaccount credit transfer in Seven. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Seven. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from Seven. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Seven. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Seven. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Seven. |

### Hlr Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get HLR Lookup](actions/get-hlr-lookup.md) | GET | Retrieves HLR lookup details from Seven. |

### Mnp Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get MNP Lookup](actions/get-mnp-lookup.md) | GET | Retrieves MNP lookup details from Seven. |

### Number

| Action | Method | Description |
| --- | --- | --- |
| [Delete Number](actions/delete-number.md) | DELETE | Deletes an active number from Seven. |
| [Get Active Number](actions/get-active-number.md) | GET | Retrieves an active number from Seven. |
| [List Active Numbers](actions/list-active-numbers.md) | GET | Retrieves active numbers from Seven. |
| [Order a Number](actions/order-a-number.md) | POST | Creates a new number order in Seven. |
| [Update Number](actions/update-number.md) | PUT | Updates an active number in Seven. |

### Number Format

| Action | Method | Description |
| --- | --- | --- |
| [Format Number](actions/format-number.md) | GET | Retrieves formatted phone number details from Seven. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Pricing](actions/get-pricing.md) | GET | Retrieves pricing information from Seven. |

### Rcs Capability

| Action | Method | Description |
| --- | --- | --- |
| [Get RCS Capabilities](actions/get-rcs-capabilities.md) | GET | Retrieves RCS capabilities from Seven. |

### Received Sms

| Action | Method | Description |
| --- | --- | --- |
| [List Received SMS](actions/list-received-sms.md) | GET | Retrieves received SMS messages from Seven. |

### Sender Id Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Sender for Voice](actions/validate-sender-for-voice.md) | POST | Creates a voice sender validation in Seven. |

### Sent Message

| Action | Method | Description |
| --- | --- | --- |
| [List Sent Messages](actions/list-sent-messages.md) | GET | Retrieves sent messages from Seven. |

### Sms

| Action | Method | Description |
| --- | --- | --- |
| [Delete SMS](actions/delete-sms.md) | DELETE | Deletes an SMS from Seven. |
| [Send SMS](actions/send-sms.md) | POST | Creates a new SMS in Seven. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Statistics](actions/get-statistics.md) | GET | Retrieves account statistics from Seven. |

### Subaccount

| Action | Method | Description |
| --- | --- | --- |
| [Create Subaccount](actions/create-subaccount.md) | POST | Creates a new subaccount in Seven. |
| [Delete Subaccount](actions/delete-subaccount.md) | DELETE | Deletes a subaccount from Seven. |
| [List Subaccounts](actions/list-subaccounts.md) | GET | Retrieves subaccounts from Seven. |
| [Update Automatic Balance Transfer](actions/update-automatic-balance-transfer.md) | PUT | Updates automatic balance transfer in Seven. |

### Voice Call

| Action | Method | Description |
| --- | --- | --- |
| [End Call](actions/end-call.md) | PUT | Ends a voice call in Seven. |
| [Send Voice Call](actions/send-voice-call.md) | POST | Creates a new voice call in Seven. |

### Voice Message

| Action | Method | Description |
| --- | --- | --- |
| [List Voice Messages](actions/list-voice-messages.md) | GET | Retrieves voice messages from Seven. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Seven. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Seven. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Seven. |

