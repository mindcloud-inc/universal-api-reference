# Go4Clients: Native API Reference

A consolidated summary of Go4Clients's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://apidoc.go4clients.com/
- **API base URL:** `https://cloud.go4clients.com:8580`

## Authentication

### API Key

Authenticate Go4Clients requests with apiKey and apiSecret headers.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · API secret from Go4Clients Platform Settings > API Settings > General.

Send these headers with each API request:

```http
apiKey: <apiKey>
apiSecret: <apiSecret>
```

[Official authentication documentation](https://apidoc.go4clients.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Calls to Voice Campaign](actions/add-calls-to-voice-campaign.md) | `POST /api/campaigns/voice/v1.0/{{voice_campaign_id}}` | [docs](https://apidoc.go4clients.com/) |
| [Add Email to Campaign](actions/add-email-to-campaign.md) | `POST /api/campaigns/email/v1.0/{{campaignId}}` | [docs](https://apidoc.go4clients.com/) |
| [Add Personalized IVR](actions/add-personalized-ivr.md) | `POST /api/campaigns/voice/v1.0/{{voice_campaign_id}}` | [docs](https://apidoc.go4clients.com/) |
| [Add Shortlink to Campaign](actions/add-shortlink-to-campaign.md) | `POST /api/campaigns/shortlink/v1.0/{{shortlink_campaign_id}}` | [docs](https://apidoc.go4clients.com/) |
| [Create and Send Voice](actions/create-and-send-voice.md) | `POST /api/campaigns/voice/v2.0/event` | [docs](https://apidoc.go4clients.com/) |
| [Create Contact](actions/create-contact.md) | `POST /api/groupscontacts/contacts/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Create Email Campaign](actions/create-email-campaign.md) | `POST /api/campaigns/email/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [Create Group](actions/create-group.md) | `POST /api/groupscontacts/groups/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [Create Shortlink Campaign](actions/create-shortlink-campaign.md) | `POST /api/campaigns/shortlink/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Create Single Shortlink](actions/create-single-shortlink.md) | `POST /api/campaigns/shortlink/v1.0/single` | [docs](https://apidoc.go4clients.com/) |
| [Create Voice Campaign](actions/create-voice-campaign.md) | `POST /api/campaigns/voice/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Create 2FA Challenge](actions/create2-fa-challenge.md) | `POST /api/tfa/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Get Balance](actions/get-balance.md) | `GET /api/balance/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Get Email Campaign](actions/get-email-campaign.md) | `GET /api/campaigns/email/v1.0/{{campaignId}}` | [docs](https://apidoc.go4clients.com/) |
| [Get Group](actions/get-group.md) | `GET /api/groupscontacts/groups/v1.0/{{groupId}}` | [docs](https://apidoc.go4clients.com/) |
| [Get Shortlink Analytics](actions/get-shortlink-analytics.md) | `GET /api/analytics/shortlink/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Get SMS Pricing](actions/get-sms-pricing.md) | `GET /api/pricing/v1.0/sms` | [docs](https://apidoc.go4clients.com/) |
| [Get Voice Analytics](actions/get-voice-analytics.md) | `GET /api/analytics/voice/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Get Voice Pricing](actions/get-voice-pricing.md) | `GET /api/pricing/v1.0/voice` | [docs](https://apidoc.go4clients.com/) |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | `GET /api/blacklist/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/groupscontacts/contacts/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [List Groups](actions/list-groups.md) | `GET /api/groupscontacts/groups/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [Number Lookup](actions/number-lookup.md) | `GET /api/lookup/v1.0/{{phoneNumber}}` | [docs](https://apidoc.go4clients.com/) |
| [Search Blacklist Entries](actions/search-blacklist-entries.md) | `GET /api/blacklist/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [Search Contacts](actions/search-contacts.md) | `GET /api/groupscontacts/contacts/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Update Contact](actions/update-contact.md) | `PUT /api/groupscontacts/contacts/v1.0` | [docs](https://apidoc.go4clients.com/) |
| [Update Email Campaign](actions/update-email-campaign.md) | `PUT /api/campaigns/email/v1.0/{{campaignId}}` | [docs](https://apidoc.go4clients.com/) |
| [Update Group](actions/update-group.md) | `PUT /api/groupscontacts/groups/v1.0/` | [docs](https://apidoc.go4clients.com/) |
| [Validate 2FA Challenge](actions/validate2-fa-challenge.md) | `POST /api/tfa/v1.0/validate` |  |
