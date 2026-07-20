# Acumbamail: Native API Reference

A consolidated summary of Acumbamail's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://acumbamail.com/apidoc/
- **API base URL:** `https://acumbamail.com/api/1`

## Authentication

### API Key

Use your Acumbamail auth token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://acumbamail.com/apidoc/)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | `POST /addSubscriber/` | [docs](https://acumbamail.com/apidoc/function/addSubscriber/) |
| [Batch Add Subscribers](actions/batch-add-subscribers.md) | `POST /batchAddSubscribers/` | [docs](https://acumbamail.com/apidoc/function/batchAddSubscribers/) |
| [Configure List Webhook](actions/configure-list-webhook.md) | `POST /configListWebhook/` | [docs](https://acumbamail.com/apidoc/function/configListWebhook/) |
| [Create Campaign](actions/create-campaign.md) | `POST /createCampaign/` | [docs](https://acumbamail.com/apidoc/function/createCampaign/) |
| [Create List](actions/create-list.md) | `POST /createList/` | [docs](https://acumbamail.com/apidoc/function/createList/) |
| [Delete Subscriber](actions/delete-subscriber.md) | `POST /deleteSubscriber/` | [docs](https://acumbamail.com/apidoc/function/deleteSubscriber/) |
| [Get Campaign Basic Information](actions/get-campaign-basic-information.md) | `POST /getCampaignBasicInformation/` | [docs](https://acumbamail.com/apidoc/function/getCampaignBasicInformation/) |
| [Get Campaign Total Information](actions/get-campaign-total-information.md) | `POST /getCampaignTotalInformation/` | [docs](https://acumbamail.com/apidoc/function/getCampaignTotalInformation/) |
| [Get List Stats](actions/get-list-stats.md) | `POST /getListStats/` | [docs](https://acumbamail.com/apidoc/function/getListStats/) |
| [Get List Webhook](actions/get-list-webhook.md) | `POST /getListWebhook/` | [docs](https://acumbamail.com/apidoc/function/getListWebhook/) |
| [Get Subscriber Details](actions/get-subscriber-details.md) | `POST /getSubscriberDetails/` | [docs](https://acumbamail.com/apidoc/function/getSubscriberDetails/) |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | `POST /getCampaignClicks/` | [docs](https://acumbamail.com/apidoc/function/getCampaignClicks/) |
| [List Campaign Links](actions/list-campaign-links.md) | `POST /getCampaignLinks/` | [docs](https://acumbamail.com/apidoc/function/getCampaignLinks/) |
| [List Campaigns](actions/list-campaigns.md) | `POST /getCampaigns/` | [docs](https://acumbamail.com/apidoc/function/getCampaigns/) |
| [List Forms](actions/list-forms.md) | `POST /getForms/` | [docs](https://acumbamail.com/apidoc/function/getForms/) |
| [List List Segments](actions/list-list-segments.md) | `POST /getListSegments/` | [docs](https://acumbamail.com/apidoc/function/getListSegments/) |
| [List Lists](actions/list-lists.md) | `POST /getLists/` | [docs](https://acumbamail.com/apidoc/function/getLists/) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `POST /getSMSCampaigns/` | [docs](https://acumbamail.com/apidoc/function/getSMSCampaigns/) |
| [List Subscribers](actions/list-subscribers.md) | `POST /getSubscribers/` | [docs](https://acumbamail.com/apidoc/function/getSubscribers/) |
| [List Templates](actions/list-templates.md) | `POST /getTemplates/` | [docs](https://acumbamail.com/apidoc/function/getTemplates/) |
| [Search Subscriber](actions/search-subscriber.md) | `POST /searchSubscriber/` | [docs](https://acumbamail.com/apidoc/function/searchSubscriber/) |
| [Send SMS](actions/send-sms.md) | `POST /sendSMS/` | [docs](https://acumbamail.com/apidoc/function/sendSMS/) |
| [Send Template Campaign](actions/send-template-campaign.md) | `POST /sendTemplateCampaign/` | [docs](https://acumbamail.com/apidoc/function/sendTemplateCampaign/) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /unsubscribeSubscriber/` | [docs](https://acumbamail.com/apidoc/function/unsubscribeSubscriber/) |
