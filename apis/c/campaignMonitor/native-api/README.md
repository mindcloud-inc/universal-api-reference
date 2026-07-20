# Campaign Monitor: Native API Reference

A consolidated summary of Campaign Monitor's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.campaignmonitor.com/api/
- **API base URL:** `https://api.createsend.com/api/v3.3`

## Authentication

### OAuth 2.0

Connect Campaign Monitor with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.createsend.com/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.createsend.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `AdministerAccount,ManageLists,ImportSubscribers,CreateCampaigns,SendCampaigns,ViewReports,ViewSubscribersInReports,ManageTemplates`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.createsend.com/oauth/token.

[Official authentication documentation](https://www.campaignmonitor.com/api/v3-3/getting-started/)

### Basic

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.campaignmonitor.com/api/v3-3/getting-started/#authenticating-api-key)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | `POST /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/#adding-a-subscriber) |
| [Create Draft Campaign](actions/create-draft-campaign.md) | `POST /campaigns/:clientId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/#creating-draft-campaign) |
| [Create List](actions/create-list.md) | `POST /lists/:clientId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#creating-a-list) |
| [Create Segment](actions/create-segment.md) | `POST /segments/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/#creating-a-segment) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/:campaignId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/#deleting-a-campaign) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#deleting-a-list) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/#deleting-a-segment) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/#deleting-a-subscriber) |
| [Get Campaign Summary](actions/get-campaign-summary.md) | `GET /campaigns/:campaignId/summary.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/#campaign-summary-2) |
| [Get Client Details](actions/get-client-details.md) | `GET /clients/:clientId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-clients-details) |
| [Get List Details](actions/get-list-details.md) | `GET /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#list-details) |
| [Get List Stats](actions/get-list-stats.md) | `GET /lists/:listId/stats.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#list-stats) |
| [Get Segment Details](actions/get-segment-details.md) | `GET /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/#getting-segments-details) |
| [Get Subscriber Details](actions/get-subscriber-details.md) | `GET /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/#getting-a-subscribers-details) |
| [List Active Subscribers](actions/list-active-subscribers.md) | `GET /lists/:listId/active.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#active-subscribers-2) |
| [List Bounced Subscribers](actions/list-bounced-subscribers.md) | `GET /lists/:listId/bounced.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#bounced-subscribers-2) |
| [List Clients](actions/list-clients.md) | `GET /clients.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /lists/:listId/customfields.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#list-custom-fields) |
| [List Deleted Subscribers](actions/list-deleted-subscribers.md) | `GET /lists/:listId/deleted.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#deleted-subscribers-2) |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | `GET /clients/:clientId/drafts.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-draft-campaigns-3) |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | `GET /clients/:clientId/scheduled.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-scheduled-campaigns-2) |
| [List Segments](actions/list-segments.md) | `GET /clients/:clientId/segments.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-segments) |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | `GET /clients/:clientId/campaigns.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-sent-campaigns-2) |
| [List Subscriber History](actions/list-subscriber-history.md) | `GET /subscribers/:listId/history.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/#getting-subscribers-history) |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | `GET /clients/:clientId/lists.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-subscriber-lists) |
| [List Templates](actions/list-templates.md) | `GET /clients/:clientId/templates.json` | [docs](https://www.campaignmonitor.com/api/v3-3/clients/#getting-templates) |
| [List Unconfirmed Subscribers](actions/list-unconfirmed-subscribers.md) | `GET /lists/:listId/unconfirmed.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#unconfirmed-subscribers-2) |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | `GET /lists/:listId/unsubscribed.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#unsubscribed-subscribers-2) |
| [Send Draft Campaign](actions/send-draft-campaign.md) | `POST /campaigns/:campaignId/send.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/#sending-draft-campaign) |
| [Update List](actions/update-list.md) | `PUT /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/#updating-a-list) |
| [Update Segment](actions/update-segment.md) | `PUT /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/#updating-a-segment) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/#updating-a-subscriber) |
