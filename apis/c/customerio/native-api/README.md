# Customer.io: Native API Reference

A consolidated summary of Customer.io's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.customer.io/integrations/api/app/
- **OpenAPI specification:** https://docs.customer.io/files/journeys-app.json
- **API base URL:** `https://api.customer.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.customer.io/accounts-and-workspaces/managing-credentials/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `workspaces`. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–30000). Use `start` in the query string as the pagination cursor.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Broadcast](actions/get-broadcast.md) | `GET /v1/broadcasts/:broadcast_id` | [docs](https://docs.customer.io/integrations/api/app/#tag/Broadcasts/operation/getBroadcast) |
| [Get Broadcast Metrics](actions/get-broadcast-metrics.md) | `GET /v1/broadcasts/:broadcast_id/metrics` | [docs](https://docs.customer.io/integrations/api/app/#tag/Broadcasts/operation/broadcastMetrics) |
| [Get Campaign](actions/get-campaign.md) | `GET /v1/campaigns/:campaign_id` | [docs](https://docs.customer.io/integrations/api/app/#tag/Campaigns/operation/getCampaigns) |
| [Get Campaign Metrics](actions/get-campaign-metrics.md) | `GET /v1/campaigns/:campaign_id/metrics` | [docs](https://docs.customer.io/integrations/api/app/#tag/Campaigns/operation/campaignMetrics) |
| [Get Newsletter](actions/get-newsletter.md) | `GET /v1/newsletters/:newsletter_id` | [docs](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/getNewsletters) |
| [Get Newsletter Metrics](actions/get-newsletter-metrics.md) | `GET /v1/newsletters/:newsletter_id/metrics` | [docs](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/getNewsletterMetrics) |
| [Get Segment](actions/get-segment.md) | `GET /v1/segments/:segment_id` | [docs](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/getSegment) |
| [Get Segment Customer Count](actions/get-segment-customer-count.md) | `GET /v1/segments/:segment_id/customer_count` | [docs](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/getSegmentCount) |
| [Get Transactional Message](actions/get-transactional-message.md) | `GET /v1/transactional/:transactional_id` | [docs](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/getTransactional) |
| [Get Transactional Message Deliveries](actions/get-transactional-message-deliveries.md) | `GET /v1/transactional/:transactional_id/messages` | [docs](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/transactionalMessages) |
| [Get Transactional Message Metrics](actions/get-transactional-message-metrics.md) | `GET /v1/transactional/:transactional_id/metrics` | [docs](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/transactionalMetrics) |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /v1/broadcasts` | [docs](https://docs.customer.io/integrations/api/app/#tag/Broadcasts/operation/listBroadcasts) |
| [List Campaigns](actions/list-campaigns.md) | `GET /v1/campaigns` | [docs](https://docs.customer.io/integrations/api/app/#tag/Campaigns/operation/listCampaigns) |
| [List Customer Activities](actions/list-customer-activities.md) | `GET /v1/customers/:customer_id/activities` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonActivities) |
| [List Customer Attributes](actions/list-customer-attributes.md) | `GET /v1/customers/:customer_id/attributes` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonAttributes) |
| [List Customer Messages](actions/list-customer-messages.md) | `GET /v1/customers/:customer_id/messages` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonMessages) |
| [List Customer Segments](actions/list-customer-segments.md) | `GET /v1/customers/:customer_id/segments` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonSegments) |
| [List Customer Subscription Preferences](actions/list-customer-subscription-preferences.md) | `GET /v1/customers/:customer_id/subscription_preferences` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonSubscriptionPreferences) |
| [List Customers, Attributes, and Devices](actions/list-customers-attributes-and-devices.md) | `POST /v1/customers/attributes` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleById) |
| [List Customers by Email](actions/list-customers-by-email.md) | `GET /v1/customers` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleEmail) |
| [List Customers in a Segment](actions/list-customers-in-segment.md) | `GET /v1/segments/:segment_id/membership` | [docs](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/getSegmentMembership) |
| [List Newsletters](actions/list-newsletters.md) | `GET /v1/newsletters` | [docs](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/listNewsletters) |
| [List Segments](actions/list-segments.md) | `GET /v1/segments` | [docs](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/listSegments) |
| [List Subscription Topics](actions/list-subscription-topics.md) | `GET /v1/subscription_topics` | [docs](https://docs.customer.io/integrations/api/app/#tag/Subscription%20Center/operation/getTopics) |
| [List Transactional Messages](actions/list-transactional-messages.md) | `GET /v1/transactional` | [docs](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/listTransactional) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://docs.customer.io/integrations/api/app/#tag/Workspaces/operation/listWorkspaces) |
| [Search Customers](actions/search-customers.md) | `POST /v1/customers` | [docs](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleFilter) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /v1/send/email` | [docs](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendEmail) |
| [Send Transactional Inbox Message](actions/send-transactional-inbox-message.md) | `POST /v1/send/inbox_message` | [docs](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendInboxMessage) |
| [Send Transactional Push](actions/send-transactional-push.md) | `POST /v1/send/push` | [docs](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendPush) |
| [Send Transactional SMS](actions/send-transactional-sms.md) | `POST /v1/send/sms` | [docs](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendSMS) |
