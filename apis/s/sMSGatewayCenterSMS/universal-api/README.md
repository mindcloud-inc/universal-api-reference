# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1775238965417.png" alt="SMSGatewayCenter SMS logo" width="28" height="28"> SMSGatewayCenter SMS: Universal API

Send SMS, WhatsApp, and voice messages, manage messaging campaigns, and retrieve account profile data with SMSGatewayCenter.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSGatewayCenterSMS/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsgatewaycenter.com/
- **Vendor API docs:** https://www.smsgatewaycenter.com/developer-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read Profile](actions/read-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account Status

| Action | Method | Description |
| --- | --- | --- |
| [Read Account Status](actions/read-account-status.md) | GET |  |

### Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [Activity Logs](actions/activity-logs.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Read API Key](actions/read-api-key.md) | GET |  |

### Connected Device

| Action | Method | Description |
| --- | --- | --- |
| [Read Connected Devices](actions/read-connected-devices.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Read Contacts](actions/read-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Credit History

| Action | Method | Description |
| --- | --- | --- |
| [Read Credit History](actions/read-credit-history.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Read Groups](actions/read-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Notification Settings

| Action | Method | Description |
| --- | --- | --- |
| [Read Notification Settings](actions/read-notification-settings.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Read Profile](actions/read-profile.md) | GET |  |

### Rate Plan

| Action | Method | Description |
| --- | --- | --- |
| [Read Rate Plan](actions/read-rate-plan.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Read Webhooks](actions/read-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

