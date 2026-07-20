# <img src="https://images.mindcloud.co/apps/icons/tel-tel_1776099613449.png" alt="TelTel logo" width="28" height="28"> TelTel: Universal API

TelTel provides REST APIs for managing telecom account data including users, devices, calls, SMS, contacts, phone numbers, number lookup, and autodialer resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/telTel/latest
- **Category:** Support / Contact Center
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teltel.io
- **Vendor API docs:** https://doc.teltel.io/en/integration-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List SMS Campaign Actions](actions/list-sms-campaign-actions.md) | GET | Retrieves SMS campaign action history from TelTel. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a click-to-call request in TelTel. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from your TelTel account. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Campaign](actions/create-sms-campaign.md) | POST | Creates a new SMS campaign in TelTel. |
| [Get Autodialer](actions/get-autodialer.md) | GET | Retrieves an autodialer campaign from TelTel. |
| [Get SMS Campaign](actions/get-sms-campaign.md) | GET | Retrieves an SMS campaign from TelTel. |
| [List Autodialers](actions/list-autodialers.md) | GET | Retrieves autodialer campaigns from your TelTel account. |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET | Retrieves SMS campaigns from your TelTel account. |
| [Run SMS Campaign Action](actions/run-sms-campaign-action.md) | PUT | Performs an action on an SMS campaign in TelTel. |
| [Update SMS Campaign](actions/update-sms-campaign.md) | PUT | Updates an existing SMS campaign in TelTel. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in TelTel. |
| [Create Contacts](actions/create-contacts.md) | POST | Creates multiple new contacts in TelTel. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a single contact from TelTel. |
| [List Contact Group Contacts](actions/list-contact-group-contacts.md) | GET | Retrieves contacts from a TelTel contact group. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your TelTel account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in TelTel. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Devices](actions/get-devices.md) | GET | Retrieves devices from your TelTel account. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Group](actions/create-contact-group.md) | POST | Creates a new contact group in TelTel. |
| [Get Contact Group](actions/get-contact-group.md) | GET | Retrieves a contact group from TelTel. |
| [List Contact Groups](actions/list-contact-groups.md) | GET | Retrieves contact groups from your TelTel account. |
| [Update Contact Group](actions/update-contact-group.md) | PUT | Updates an existing contact group in TelTel. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbound SMS Report](actions/get-inbound-sms-report.md) | GET | Retrieves an inbound SMS report from TelTel. |
| [Get SMS Report](actions/get-sms-report.md) | GET | Retrieves an outbound SMS report from TelTel. |
| [List Inbound SMS Reports](actions/list-inbound-sms-reports.md) | GET | Retrieves inbound SMS reports from your TelTel account. |
| [List SMS Reports](actions/list-sms-reports.md) | GET | Retrieves outbound SMS reports from your TelTel account. |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST | Sends multiple SMS messages in a single TelTel request. |
| [Send SMS](actions/send-sms.md) | POST | Sends a single SMS message in TelTel. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Number Orders](actions/list-number-orders.md) | GET | Retrieves phone number orders from your TelTel account. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Assign Phone Number To Groups](actions/assign-phone-number-to-groups.md) | PUT | Assigns a phone number to groups in TelTel. |
| [Assign Phone Number To Users](actions/assign-phone-number-to-users.md) | PUT | Assigns a phone number to users in TelTel. |
| [Get Available Number Country](actions/get-available-number-country.md) | GET | Retrieves available number country details from TelTel. |
| [Get Phone Number](actions/get-phone-number.md) | GET | Retrieves a phone number from TelTel. |
| [List Available Number Countries](actions/list-available-number-countries.md) | GET | Retrieves available phone number countries from TelTel. |
| [List Available Number Price Groups](actions/list-available-number-price-groups.md) | GET | Retrieves available phone number price groups from TelTel. |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from your TelTel account. |
| [Lookup Phone Numbers](actions/lookup-phone-numbers.md) | GET | Looks up phone numbers in TelTel. |
| [Update Phone Number](actions/update-phone-number.md) | PUT | Updates an existing phone number in TelTel. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get User Statuses](actions/get-user-statuses.md) | GET | Retrieves user statuses from your TelTel account. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves account balance details from your TelTel account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves users from your TelTel account. |

