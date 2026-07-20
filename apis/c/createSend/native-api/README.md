# CreateSend: Native API Reference

A consolidated summary of CreateSend's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.campaignmonitor.com/api/
- **API base URL:** `https://api.createsend.com/api/v3.3`

## Authentication

### API Key (Basic Auth)

Authenticate with HTTP Basic auth. Put the Campaign Monitor API key in the username field. Leave the password blank if the UI allows it, or use a dummy value like x. Do not use the Campaign Monitor Client ID for the test connection.

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

[Official authentication documentation](https://www.campaignmonitor.com/api/v3-3/getting-started/)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | `POST /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/) |
| [Create Draft Campaign](actions/create-draft-campaign.md) | `POST /campaigns/:clientId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/) |
| [Create List](actions/create-list.md) | `POST /lists/:clientId.json` | [docs](https://www.campaignmonitor.com/api/lists/) |
| [Create Segment](actions/create-segment.md) | `POST /segments/:listId.json` | [docs](https://www.campaignmonitor.com/api/segments/) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/:campaignId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/lists/) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/) |
| [Get Campaign Summary](actions/get-campaign-summary.md) | `GET /campaigns/:campaignId/summary.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/) |
| [Get Client Details](actions/get-client-details.md) | `GET /clients/:clientId.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [Get List Details](actions/get-list-details.md) | `GET /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [Get List Stats](actions/get-list-stats.md) | `GET /lists/:listId/stats.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [Get Segment Details](actions/get-segment-details.md) | `GET /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/segments/) |
| [Get Subscriber Details](actions/get-subscriber-details.md) | `GET /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/) |
| [Get Subscriber History](actions/get-subscriber-history.md) | `GET /subscribers/:listId/history.json` | [docs](https://www.campaignmonitor.com/api/v3-3/subscribers/) |
| [List Active Subscribers](actions/list-active-subscribers.md) | `GET /lists/:listId/active.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [List Bounced Subscribers](actions/list-bounced-subscribers.md) | `GET /lists/:listId/bounced.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [List Clients](actions/list-clients.md) | `GET /clients.json` | [docs](https://www.campaignmonitor.com/api/v3-3/account/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /lists/:listId/customfields.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [List Deleted Subscribers](actions/list-deleted-subscribers.md) | `GET /lists/:listId/deleted.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | `GET /clients/:clientId/drafts.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | `GET /clients/:clientId/scheduled.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Segments](actions/list-segments.md) | `GET /clients/:clientId/segments.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | `GET /clients/:clientId/campaigns.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | `GET /clients/:clientId/lists.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Templates](actions/list-templates.md) | `GET /clients/:clientId/templates.json` | [docs](https://www.campaignmonitor.com/api/clients/) |
| [List Unconfirmed Subscribers](actions/list-unconfirmed-subscribers.md) | `GET /lists/:listId/unconfirmed.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | `GET /lists/:listId/unsubscribed.json` | [docs](https://www.campaignmonitor.com/api/v3-3/lists/) |
| [Send Draft Campaign](actions/send-draft-campaign.md) | `POST /campaigns/:campaignId/send.json` | [docs](https://www.campaignmonitor.com/api/v3-3/campaigns/) |
| [Update List](actions/update-list.md) | `PUT /lists/:listId.json` | [docs](https://www.campaignmonitor.com/api/lists/) |
| [Update Segment](actions/update-segment.md) | `PUT /segments/:segmentId.json` | [docs](https://www.campaignmonitor.com/api/v3-3/segments/) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/:listId.json` | [docs](https://www.campaignmonitor.com/api/subscribers/) |
