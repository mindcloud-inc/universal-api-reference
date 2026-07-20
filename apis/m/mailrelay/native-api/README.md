# Mailrelay: Native API Reference

A consolidated summary of Mailrelay's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.mailrelay.com/
- **OpenAPI specification:** https://apidocs.mailrelay.com/openapi.json
- **API base URL:** `https://{accountDomain}/api/v1`

## Authentication

### API Key

Connect Mailrelay with your account domain and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Account Domain:** `accountDomain` · required · Your Mailrelay account domain, for example `youraccount.ipzmarketing.com`.

Send these headers with each API request:

```http
X-AUTH-TOKEN: <apiKey>
```

[Official authentication documentation](https://apidocs.mailrelay.com/)

## Pagination

Use `per_page` in the query string to set the page size (default 30; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Subscribers](actions/bulk-update-subscribers.md) | `PATCH subscribers/bulk_update` | [docs](https://apidocs.mailrelay.com/) |
| [Create Campaign](actions/create-campaign.md) | `POST campaigns` | [docs](https://apidocs.mailrelay.com/) |
| [Create Group](actions/create-group.md) | `POST groups` | [docs](https://apidocs.mailrelay.com/) |
| [Create Sender](actions/create-sender.md) | `POST senders` | [docs](https://apidocs.mailrelay.com/) |
| [Create Subscriber](actions/create-subscriber.md) | `POST subscribers` | [docs](https://apidocs.mailrelay.com/) |
| [Get Campaign](actions/get-campaign.md) | `GET campaigns/:id` | [docs](https://apidocs.mailrelay.com/) |
| [Get Group](actions/get-group.md) | `GET groups/:id` | [docs](https://apidocs.mailrelay.com/) |
| [Get Package Info](actions/get-package-info.md) | `GET package` | [docs](https://apidocs.mailrelay.com/) |
| [Get Sent Campaign](actions/get-sent-campaign.md) | `GET sent_campaigns/:id` | [docs](https://apidocs.mailrelay.com/) |
| [Get Stats Summary](actions/get-stats-summary.md) | `GET stats` | [docs](https://apidocs.mailrelay.com/) |
| [Get Subscriber](actions/get-subscriber.md) | `GET subscribers/:id` | [docs](https://apidocs.mailrelay.com/) |
| [List Campaigns](actions/list-campaigns.md) | `GET campaigns` | [docs](https://apidocs.mailrelay.com/) |
| [List Groups](actions/list-groups.md) | `GET groups` | [docs](https://apidocs.mailrelay.com/) |
| [List Senders](actions/list-senders.md) | `GET senders` | [docs](https://apidocs.mailrelay.com/) |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | `GET sent_campaigns` | [docs](https://apidocs.mailrelay.com/) |
| [List Subscribers](actions/list-subscribers.md) | `GET subscribers` | [docs](https://apidocs.mailrelay.com/) |
| [Ping](actions/ping.md) | `GET ping` | [docs](https://apidocs.mailrelay.com/) |
| [Send Campaign](actions/send-campaign.md) | `POST campaigns/:id/send_all` | [docs](https://apidocs.mailrelay.com/) |
| [Send Campaign Test](actions/send-campaign-test.md) | `POST campaigns/:id/send_test` | [docs](https://apidocs.mailrelay.com/) |
| [Send Email](actions/send-email.md) | `POST send_emails` | [docs](https://apidocs.mailrelay.com/) |
| [Sync Subscriber](actions/sync-subscriber.md) | `POST subscribers/sync` | [docs](https://apidocs.mailrelay.com/) |
| [Update Campaign](actions/update-campaign.md) | `PATCH campaigns/:id` | [docs](https://apidocs.mailrelay.com/) |
| [Update Group](actions/update-group.md) | `PATCH groups/:id` | [docs](https://apidocs.mailrelay.com/) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH subscribers/:id` | [docs](https://apidocs.mailrelay.com/) |
