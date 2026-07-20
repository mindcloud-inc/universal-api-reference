# <img src="https://images.mindcloud.co/apps/icons/smsmode_1776102269993.png" alt="smsmode logo" width="28" height="28"> smsmode: Universal API

smsmode provides REST APIs for SMS, RCS, account resources, credentials, consumption, transfers, and number lookup.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smsmode/latest
- **Category:** Marketing
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsmode.com/
- **Vendor API docs:** https://dev.smsmode.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organisations](actions/list-organisations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential](actions/create-credential.md) | POST |  |
| [Delete Credential](actions/delete-credential.md) | DELETE |  |
| [Get Credential](actions/get-credential.md) | GET |  |
| [List Credentials](actions/list-credentials.md) | GET |  |
| [Update Credential](actions/update-credential.md) | PUT |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled RCS Campaign](actions/cancel-scheduled-rcs-campaign.md) | DELETE |  |
| [Cancel Scheduled SMS Campaign](actions/cancel-scheduled-sms-campaign.md) | DELETE |  |
| [Get RCS Campaign](actions/get-rcs-campaign.md) | GET |  |
| [Get SMS Campaign](actions/get-sms-campaign.md) | GET |  |
| [List RCS Campaigns](actions/list-rcs-campaigns.md) | GET |  |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET |  |
| [Send RCS Campaign](actions/send-rcs-campaign.md) | POST |  |
| [Send SMS Campaign](actions/send-sms-campaign.md) | POST |  |
| [Update Scheduled RCS Campaign](actions/update-scheduled-rcs-campaign.md) | PUT |  |
| [Update Scheduled SMS Campaign](actions/update-scheduled-sms-campaign.md) | PUT |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST |  |
| [Get Channel](actions/get-channel.md) | GET |  |
| [List Channels](actions/list-channels.md) | GET |  |
| [Update Channel](actions/update-channel.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled RCS Message](actions/cancel-scheduled-rcs-message.md) | DELETE |  |
| [Cancel Scheduled SMS Message](actions/cancel-scheduled-sms-message.md) | DELETE |  |
| [Get RCS Message](actions/get-rcs-message.md) | GET |  |
| [Get SMS Message](actions/get-sms-message.md) | GET |  |
| [List RCS Messages](actions/list-rcs-messages.md) | GET |  |
| [List SMS Messages](actions/list-sms-messages.md) | GET |  |
| [Send RCS Message](actions/send-rcs-message.md) | POST |  |
| [Send SMS Message](actions/send-sms-message.md) | POST |  |
| [Update Scheduled RCS Message](actions/update-scheduled-rcs-message.md) | PUT |  |
| [Update Scheduled SMS Message](actions/update-scheduled-sms-message.md) | PUT |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Create Organisation](actions/create-organisation.md) | POST |  |
| [Get Organisation](actions/get-organisation.md) | GET |  |
| [List Organisations](actions/list-organisations.md) | GET |  |
| [Update Organisation](actions/update-organisation.md) | PUT |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Number](actions/lookup-number.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transfer](actions/create-transfer.md) | POST |  |
| [Get Consumption](actions/get-consumption.md) | GET |  |
| [Get Transfer](actions/get-transfer.md) | GET |  |
| [List Consumptions](actions/list-consumptions.md) | GET |  |
| [List Transfers](actions/list-transfers.md) | GET |  |

