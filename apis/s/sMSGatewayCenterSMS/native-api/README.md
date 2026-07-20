# SMSGatewayCenter SMS: Native API Reference

A consolidated summary of SMSGatewayCenter SMS's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.smsgatewaycenter.com/developer-api/
- **API base URL:** `https://unify.smsgateway.center`

## Authentication

### API Key

Authenticate SMSGatewayCenter with the API key generated from the user control panel.

### Credentials

- **API Key:** `apiKey` · required
- **User ID:** `userId` · required · Registered SMSGatewayCenter username required alongside the API key for API requests.

Send these headers with each API request:

```http
apiKey: <apiKey>
```

[Official authentication documentation](https://www.smsgatewaycenter.com/developer-api/authentication/)

## API conventions

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activity Logs](actions/activity-logs.md) | `GET /SMSApi/activity/read` | [docs](https://www.smsgatewaycenter.com/developer-api/activity/) |
| [Create Contact](actions/create-contact.md) | `POST /SMSApi/contact/create` | [docs](https://www.smsgatewaycenter.com/developer-api/create-contact/) |
| [Create Group](actions/create-group.md) | `POST /SMSApi/group/create` | [docs](https://www.smsgatewaycenter.com/developer-api/create-group/) |
| [Create Webhook](actions/create-webhook.md) | `POST /SMSApi/webhook/create` | [docs](https://www.smsgatewaycenter.com/developer-api/create-webhook/) |
| [Delete Contact](actions/delete-contact.md) | `POST /SMSApi/contact/delete` | [docs](https://www.smsgatewaycenter.com/developer-api/delete-contact/) |
| [Delete Group](actions/delete-group.md) | `POST /SMSApi/group/delete` | [docs](https://www.smsgatewaycenter.com/developer-api/delete-group/) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /SMSApi/webhook/delete` | [docs](https://www.smsgatewaycenter.com/developer-api/delete-webhook/) |
| [Read Account Status](actions/read-account-status.md) | `GET /SMSApi/account/readstatus` | [docs](https://www.smsgatewaycenter.com/developer-api/read-account-status/) |
| [Read API Key](actions/read-api-key.md) | `GET /SMSApi/apikey/read` | [docs](https://www.smsgatewaycenter.com/developer-api/read-api-key/) |
| [Read Connected Devices](actions/read-connected-devices.md) | `GET /SMSApi/security/connectedDevices` | [docs](https://www.smsgatewaycenter.com/developer-api/connectedDevices/) |
| [Read Contacts](actions/read-contacts.md) | `GET /SMSApi/contact/read` | [docs](https://www.smsgatewaycenter.com/developer-api/read-contact/) |
| [Read Credit History](actions/read-credit-history.md) | `POST /SMSApi/account/readcredithistory` | [docs](https://www.smsgatewaycenter.com/developer-api/read-credit-history/) |
| [Read Groups](actions/read-groups.md) | `GET /SMSApi/group/read` | [docs](https://www.smsgatewaycenter.com/developer-api/read-group/) |
| [Read Notification Settings](actions/read-notification-settings.md) | `GET /SMSApi/notifications/read` | [docs](https://www.smsgatewaycenter.com/developer-api/notification/) |
| [Read Profile](actions/read-profile.md) | `GET /SMSApi/account/readprofile` | [docs](https://www.smsgatewaycenter.com/developer-api/read-profile/) |
| [Read Rate Plan](actions/read-rate-plan.md) | `GET /SMSApi/rateplan/read` | [docs](https://www.smsgatewaycenter.com/developer-api/rateplan/) |
| [Read Webhooks](actions/read-webhooks.md) | `GET /SMSApi/webhook/read` | [docs](https://www.smsgatewaycenter.com/developer-api/read-webhook/) |
| [Update Contact](actions/update-contact.md) | `POST /SMSApi/contact/update` | [docs](https://www.smsgatewaycenter.com/developer-api/update-contact/) |
| [Update Group](actions/update-group.md) | `POST /SMSApi/group/update` | [docs](https://www.smsgatewaycenter.com/developer-api/update-group/) |
| [Update Webhook](actions/update-webhook.md) | `POST /SMSApi/webhook/update` | [docs](https://www.smsgatewaycenter.com/developer-api/update-webhook/) |
