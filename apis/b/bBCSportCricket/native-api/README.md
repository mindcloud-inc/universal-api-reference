# BBC Sport - Cricket: Native API Reference

A consolidated summary of BBC Sport - Cricket's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://feeds.bbci.co.uk/sport/cricket/rss.xml
- **API base URL:** `https://feeds.bbci.co.uk`

## Authentication

### No authentication

BBC Sport cricket RSS feed endpoints used by this app are publicly accessible.

This API does not require request authentication.

[Official authentication documentation](https://feeds.bbci.co.uk/sport/cricket/rss.xml)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Afghanistan Cricket Headlines](actions/list-afghanistan-cricket-headlines.md) | `GET /sport/cricket/teams/afghanistan/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/afghanistan/rss.xml) |
| [List Australia Cricket Headlines](actions/list-australia-cricket-headlines.md) | `GET /sport/cricket/teams/australia/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/australia/rss.xml) |
| [List Bangladesh Cricket Headlines](actions/list-bangladesh-cricket-headlines.md) | `GET /sport/cricket/teams/bangladesh/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/bangladesh/rss.xml) |
| [List County Cricket Headlines](actions/list-county-cricket-headlines.md) | `GET /sport/cricket/counties/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/counties/rss.xml) |
| [List Cricket Headlines](actions/list-cricket-headlines.md) | `GET /sport/cricket/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/rss.xml) |
| [List England Cricket Headlines](actions/list-england-cricket-headlines.md) | `GET /sport/cricket/teams/england/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/england/rss.xml) |
| [List England Women Cricket Headlines](actions/list-england-women-cricket-headlines.md) | `GET /sport/cricket/teams/england-women/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/england-women/rss.xml) |
| [List Franchise Cricket Headlines](actions/list-franchise-cricket-headlines.md) | `GET /sport/cricket/franchise-cricket/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/franchise-cricket/rss.xml) |
| [List India Cricket Headlines](actions/list-india-cricket-headlines.md) | `GET /sport/cricket/teams/india/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/india/rss.xml) |
| [List Ireland Cricket Headlines](actions/list-ireland-cricket-headlines.md) | `GET /sport/cricket/teams/ireland/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/ireland/rss.xml) |
| [List New Zealand Cricket Headlines](actions/list-new-zealand-cricket-headlines.md) | `GET /sport/cricket/teams/new-zealand/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/new-zealand/rss.xml) |
| [List Pakistan Cricket Headlines](actions/list-pakistan-cricket-headlines.md) | `GET /sport/cricket/teams/pakistan/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/pakistan/rss.xml) |
| [List Scotland Cricket Headlines](actions/list-scotland-cricket-headlines.md) | `GET /sport/cricket/teams/scotland/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/scotland/rss.xml) |
| [List South Africa Cricket Headlines](actions/list-south-africa-cricket-headlines.md) | `GET /sport/cricket/teams/south-africa/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/south-africa/rss.xml) |
| [List Sri Lanka Cricket Headlines](actions/list-sri-lanka-cricket-headlines.md) | `GET /sport/cricket/teams/sri-lanka/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/sri-lanka/rss.xml) |
| [List Surrey Cricket Headlines](actions/list-surrey-cricket-headlines.md) | `GET /sport/cricket/teams/surrey/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/surrey/rss.xml) |
| [List The Hundred Headlines](actions/list-the-hundred-headlines.md) | `GET /sport/cricket/the-hundred/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/the-hundred/rss.xml) |
| [List West Indies Cricket Headlines](actions/list-west-indies-cricket-headlines.md) | `GET /sport/cricket/teams/west-indies/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/west-indies/rss.xml) |
| [List Yorkshire Cricket Headlines](actions/list-yorkshire-cricket-headlines.md) | `GET /sport/cricket/teams/yorkshire/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/yorkshire/rss.xml) |
| [List Zimbabwe Cricket Headlines](actions/list-zimbabwe-cricket-headlines.md) | `GET /sport/cricket/teams/zimbabwe/rss.xml` | [docs](https://feeds.bbci.co.uk/sport/cricket/teams/zimbabwe/rss.xml) |
