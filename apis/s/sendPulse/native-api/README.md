# SendPulse: Native API Reference

A consolidated summary of SendPulse's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://sendpulse.com/integrations/api/bulk-email
- **API base URL:** `https://api.sendpulse.com`

## Authentication

### OAuth 2.0

Connect with a SendPulse API ID and Secret.

### Credentials

- **Client ID:** `clientId` · required · Your SendPulse API ID from Account settings > API.
- **Client Secret:** `clientSecret` · required · Your SendPulse API Secret from Account settings > API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.sendpulse.com/oauth/access_token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://sendpulse.com/integrations/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Emails to Mailing List](actions/add-emails-to-mailing-list.md) | `POST /addressbooks/:mailingListId/emails` | [docs](https://sendpulse.com/integrations/api/bulk-email#add-email) |
| [Add Sender](actions/add-sender.md) | `POST /senders` | [docs](https://sendpulse.com/integrations/api/bulk-email#add-sender) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://sendpulse.com/integrations/api/bulk-email#create-campaign) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST /addressbooks` | [docs](https://sendpulse.com/integrations/api/bulk-email#create-list) |
| [Create Template](actions/create-template.md) | `POST /template` | [docs](https://sendpulse.com/integrations/api/bulk-email#create-template) |
| [Delete Emails From Mailing List](actions/delete-emails-from-mailing-list.md) | `DELETE /addressbooks/:mailingListId/emails` | [docs](https://sendpulse.com/integrations/api/bulk-email#delete-email) |
| [Get Account Information](actions/get-account-information.md) | `GET /user/info` | [docs](https://sendpulse.com/integrations/api#user-info) |
| [Get Balance Information](actions/get-balance-information.md) | `GET /balance` | [docs](https://sendpulse.com/integrations/api/bulk-email#get-balance) |
| [Get Campaign Information](actions/get-campaign-information.md) | `GET /campaigns/:campaignId` | [docs](https://sendpulse.com/integrations/api/bulk-email#campaign-info) |
| [Get Detailed Balance Information](actions/get-detailed-balance-information.md) | `GET /user/balance/detail` | [docs](https://sendpulse.com/integrations/api/bulk-email#get-balance-details) |
| [Get Mailing List Campaign Cost](actions/get-mailing-list-campaign-cost.md) | `GET /addressbooks/:mailingListId/cost` | [docs](https://sendpulse.com/integrations/api/bulk-email#campaign-cost) |
| [Get Mailing List Contact Count](actions/get-mailing-list-contact-count.md) | `GET /addressbooks/:mailingListId/emails/total` | [docs](https://sendpulse.com/integrations/api/bulk-email#get_total_addresses) |
| [Get Mailing List Information](actions/get-mailing-list-information.md) | `GET /addressbooks/:mailingListId` | [docs](https://sendpulse.com/integrations/api/bulk-email#list-info) |
| [Get Template Information](actions/get-template-information.md) | `GET /template/:templateId` | [docs](https://sendpulse.com/integrations/api/bulk-email#template-id) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://sendpulse.com/integrations/api/bulk-email#campaigns-list) |
| [List Campaigns For Mailing List](actions/list-campaigns-for-mailing-list.md) | `GET /addressbooks/:mailingListId/campaigns` | [docs](https://sendpulse.com/integrations/api/bulk-email#campaigns-list_book) |
| [List Mailing List Emails](actions/list-mailing-list-emails.md) | `GET /addressbooks/:mailingListId/emails` | [docs](https://sendpulse.com/integrations/api/bulk-email#lists-emails) |
| [List Mailing List Variables](actions/list-mailing-list-variables.md) | `GET /addressbooks/:mailingListId/variables` | [docs](https://sendpulse.com/integrations/api/bulk-email#variables) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /addressbooks` | [docs](https://sendpulse.com/integrations/api/bulk-email#lists-list) |
| [List Senders](actions/list-senders.md) | `GET /senders` | [docs](https://sendpulse.com/integrations/api/bulk-email#senders-list) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://sendpulse.com/integrations/api/bulk-email#template-list) |
| [Update Mailing List](actions/update-mailing-list.md) | `PUT /addressbooks/:mailingListId` | [docs](https://sendpulse.com/integrations/api/bulk-email#edit-list) |
| [Update Scheduled Campaign](actions/update-scheduled-campaign.md) | `PATCH /campaigns/:campaignId` | [docs](https://sendpulse.com/integrations/api/bulk-email#edit-campaign) |
| [Update Template](actions/update-template.md) | `POST /template/edit/:templateId` | [docs](https://sendpulse.com/integrations/api/bulk-email#edit-template) |
