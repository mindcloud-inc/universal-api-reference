# smsmode: Native API Reference

A consolidated summary of smsmode's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://dev.smsmode.com/
- **API base URL:** `https://rest.smsmode.com/`

## Authentication

### API Key

Use the smsmode REST API key in the X-Api-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://dev.smsmode.com/commons/v1/#section/Introduction/Authentication-and-Authorisation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Scheduled RCS Campaign](actions/cancel-scheduled-rcs-campaign.md) | `DELETE rcs/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/cancel-scheduled-campaign) |
| [Cancel Scheduled RCS Message](actions/cancel-scheduled-rcs-message.md) | `DELETE rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/cancel-scheduled-message) |
| [Cancel Scheduled SMS Campaign](actions/cancel-scheduled-sms-campaign.md) | `DELETE sms/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Campaign/operation/cancel-scheduled-campaign) |
| [Cancel Scheduled SMS Message](actions/cancel-scheduled-sms-message.md) | `DELETE sms/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Message/operation/cancel-scheduled-message) |
| [Create Channel](actions/create-channel.md) | `POST commons/v1/organisations/:organisationId/channels` | [docs](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channel-creation) |
| [Create Credential](actions/create-credential.md) | `POST commons/v1/channels/:channelId/credentials` | [docs](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credential-creation) |
| [Create Organisation](actions/create-organisation.md) | `POST commons/v1/organisations` | [docs](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisation-creation) |
| [Create Transfer](actions/create-transfer.md) | `POST commons/v1/organisations/:organisationId/transfers` | [docs](https://dev.smsmode.com/commons/v1/#tag/Transfer/operation/transfer-creation) |
| [Delete Credential](actions/delete-credential.md) | `DELETE commons/v1/channels/:channelId/credentials/:credentialId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/delete-credential) |
| [Get Channel](actions/get-channel.md) | `GET commons/v1/organisations/:organisationId/channels/:channelId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channel-details) |
| [Get Consumption](actions/get-consumption.md) | `GET commons/v1/channels/:channelId/consumptions/:consumptionId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Consumption/operation/consumption-details) |
| [Get Credential](actions/get-credential.md) | `GET commons/v1/channels/:channelId/credentials/:credentialId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credential-details) |
| [Get Organisation](actions/get-organisation.md) | `GET commons/v1/organisations/:organisationId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisation-details) |
| [Get RCS Campaign](actions/get-rcs-campaign.md) | `GET rcs/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/campaign-details) |
| [Get RCS Message](actions/get-rcs-message.md) | `GET rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/message-details) |
| [Get SMS Campaign](actions/get-sms-campaign.md) | `GET sms/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Campaign/operation/campaign-details) |
| [Get SMS Message](actions/get-sms-message.md) | `GET sms/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Message/operation/message-details) |
| [Get Transfer](actions/get-transfer.md) | `GET commons/v1/organisations/:organisationId/transfers/:transferId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Transfer/operation/transfer-details) |
| [List Channels](actions/list-channels.md) | `GET commons/v1/organisations/:organisationId/channels` | [docs](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channels-list) |
| [List Consumptions](actions/list-consumptions.md) | `GET commons/v1/channels/:channelId/consumptions` | [docs](https://dev.smsmode.com/commons/v1/#tag/Consumption/operation/consumptions-list) |
| [List Credentials](actions/list-credentials.md) | `GET commons/v1/channels/:channelId/credentials` | [docs](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credentials-list) |
| [List Organisations](actions/list-organisations.md) | `GET commons/v1/organisations` | [docs](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisations-list) |
| [List RCS Campaigns](actions/list-rcs-campaigns.md) | `GET rcs/v1/channels/:channelId/campaigns` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/campaigns-list) |
| [List RCS Messages](actions/list-rcs-messages.md) | `GET rcs/v1/channels/:channelId/campaigns/:campaignId/messages` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/messages-list) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `GET sms/v1/channels/:channelId/campaigns` | [docs](https://dev.smsmode.com/sms/v1/#tag/Campaign/operation/campaigns-list) |
| [List SMS Messages](actions/list-sms-messages.md) | `GET sms/v1/channels/:channelId/campaigns/:campaignId/messages` | [docs](https://dev.smsmode.com/sms/v1/#tag/Message/operation/messages-list) |
| [List Transfers](actions/list-transfers.md) | `GET commons/v1/organisations/:organisationId/transfers` | [docs](https://dev.smsmode.com/commons/v1/#tag/Transfer/operation/transfers-list) |
| [Lookup Number](actions/lookup-number.md) | `GET commons/v1/lookup/:msisdn` | [docs](https://dev.smsmode.com/commons/v1/#tag/Lookup/operation/number-lookup) |
| [Send RCS Campaign](actions/send-rcs-campaign.md) | `POST rcs/v1/channels/:channelId/campaigns` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/send-campaign) |
| [Send RCS Message](actions/send-rcs-message.md) | `POST rcs/v1/channels/:channelId/campaigns/:campaignId/messages` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/send-message) |
| [Send SMS Campaign](actions/send-sms-campaign.md) | `POST sms/v1/channels/:channelId/campaigns` | [docs](https://dev.smsmode.com/sms/v1/#tag/Campaign/operation/send-campaign) |
| [Send SMS Message](actions/send-sms-message.md) | `POST sms/v1/channels/:channelId/campaigns/:campaignId/messages` | [docs](https://dev.smsmode.com/sms/v1/#tag/Message/operation/send-message) |
| [Update Channel](actions/update-channel.md) | `PATCH commons/v1/organisations/:organisationId/channels/:channelId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Channel/operation/channel-update) |
| [Update Credential](actions/update-credential.md) | `PATCH commons/v1/channels/:channelId/credentials/:credentialId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Credential/operation/credential-update) |
| [Update Organisation](actions/update-organisation.md) | `PATCH commons/v1/organisations/:organisationId` | [docs](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisation-update) |
| [Update Scheduled RCS Campaign](actions/update-scheduled-rcs-campaign.md) | `PATCH rcs/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Campaign/operation/edit-scheduled-campaign) |
| [Update Scheduled RCS Message](actions/update-scheduled-rcs-message.md) | `PATCH rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/rcs/v1/#tag/Message/operation/edit-scheduled-message) |
| [Update Scheduled SMS Campaign](actions/update-scheduled-sms-campaign.md) | `PATCH sms/v1/channels/:channelId/campaigns/:campaignId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Campaign/operation/edit-scheduled-campaign) |
| [Update Scheduled SMS Message](actions/update-scheduled-sms-message.md) | `PATCH sms/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` | [docs](https://dev.smsmode.com/sms/v1/#tag/Message/operation/edit-scheduled-message) |
