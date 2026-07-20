# Zoho Campaigns: Native API Reference

A consolidated summary of Zoho Campaigns's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/campaigns/help/developers/
- **API base URL:** `https://campaigns.zoho.com/api/v1.1`

## Authentication

### OAuth 2.0

### Credentials

- **Zoho Domain:** `zohodomain` · required · Zoho Campaigns data center suffix from your app URL. Use com, eu, in, com.au, jp, ca, com.cn, or sa.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoCampaigns.campaign.ALL ZohoCampaigns.contact.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/accounts/protocol/oauth/web-server-applications.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `recent_sent_campaigns`.

## Pagination

Use `range` in the query string to set the page size. Use `fromindex` in the query string as the record offset; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add List Contacts in Bulk](actions/add-list-contacts-in-bulk.md) | `POST /addlistsubscribersinbulk` | [docs](https://www.zoho.com/campaigns/help/developers/add-contacts-existing-list.html) |
| [Add New List and Contacts](actions/add-new-list-and-contacts.md) | `POST /addlistandcontacts` | [docs](https://www.zoho.com/campaigns/help/developers/add-new-list-contact.html) |
| [Create Campaign](actions/create-campaign.md) | `POST /createCampaign` | [docs](https://www.zoho.com/campaigns/help/developers/create-campaign.html) |
| [Create Topics](actions/create-topics.md) | `POST /topics` | [docs](https://www.zoho.com/campaigns/help/developers/create-topics.html) |
| [Get Campaign Details](actions/get-campaign-details.md) | `GET /getcampaigndetails` | [docs](https://www.zoho.com/campaigns/help/developers/campaign-details.html) |
| [Get Campaign Recipients Data](actions/get-campaign-recipients-data.md) | `POST /getcampaignrecipientsdata` | [docs](https://www.zoho.com/campaigns/help/developers/campaign-recipient-data.html) |
| [Get Last Campaign Report](actions/get-last-campaign-report.md) | `POST /getlastcampaignreport` | [docs](https://www.zoho.com/campaigns/help/developers/last-campaign-report.html) |
| [Get Segment Details](actions/get-segment-details.md) | `GET /getsegmentdetails` | [docs](https://www.zoho.com/campaigns/help/developers/get-segment-details.html) |
| [Get Total Contacts](actions/get-total-contacts.md) | `GET /listsubscriberscount` | [docs](https://www.zoho.com/campaigns/help/developers/view-total-contacts.html) |
| [List Campaign Reports](actions/list-campaign-reports.md) | `GET /campaignreports` | [docs](https://www.zoho.com/campaigns/help/developers/campaign-reports.html) |
| [List Contact Fields](actions/list-contact-fields.md) | `GET /contact/allfields` | [docs](https://www.zoho.com/campaigns/help/developers/get-contact-fields.html) |
| [List Contacts](actions/list-contacts.md) | `GET /getlistsubscribers` | [docs](https://www.zoho.com/campaigns/help/developers/get-list-subscribers.html) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /getmailinglists` | [docs](https://www.zoho.com/campaigns/help/developers/get-mailing-lists.html) |
| [List Recent Campaigns](actions/list-recent-campaigns.md) | `GET /recentcampaigns` | [docs](https://www.zoho.com/campaigns/help/developers/recent-campaign.html) |
| [List Recently Sent Campaigns](actions/list-recently-sent-campaigns.md) | `GET /recentsentcampaigns` | [docs](https://www.zoho.com/campaigns/help/developers/) |
| [List Segment Contacts](actions/list-segment-contacts.md) | `GET /getsegmentcontacts` | [docs](https://www.zoho.com/campaigns/help/developers/get-segment-contacts.html) |
| [List Topics](actions/list-topics.md) | `GET /topics` | [docs](https://www.zoho.com/campaigns/help/developers/get-topics.html) |
| [Move Contact to Do Not Mail](actions/move-contact-to-do-not-mail.md) | `POST /json/contactdonotmail` | [docs](https://www.zoho.com/campaigns/help/developers/do-not-mail.html) |
| [Schedule Campaign](actions/schedule-campaign.md) | `POST /sendcampaign` | [docs](https://www.zoho.com/campaigns/help/developers/schedule-campaign.html) |
| [Send Campaign](actions/send-campaign.md) | `POST /sendcampaign` | [docs](https://www.zoho.com/campaigns/help/developers/send-campaign.html) |
| [Subscribe Contact to List](actions/subscribe-contact-to-list.md) | `POST /json/listsubscribe` | [docs](https://www.zoho.com/campaigns/help/developers/contact-subscribe.html) |
| [Unsubscribe Contact from List](actions/unsubscribe-contact-from-list.md) | `POST /json/listunsubscribe` | [docs](https://www.zoho.com/campaigns/help/developers/contact-unsubscribe.html) |
| [Update List Details](actions/update-list-details.md) | `POST /updatelistdetails` | [docs](https://www.zoho.com/campaigns/help/developers/update-list.html) |
