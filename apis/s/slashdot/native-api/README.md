# Slashdot: Native API Reference

A consolidated summary of Slashdot's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://news.slashdot.org/faq/feeds.shtml
- **API base URL:** `https://rss.slashdot.org/Slashdot/`

## Authentication

### No Authentication

Public RSS feed access for Slashdot.

This API does not require request authentication.

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml;q=0.9, text/xml;q=0.8, */*;q=0.1` |

Responses from this API use XML.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ask Slashdot Feed](actions/get-ask-slashdot-feed.md) | `GET slashdotAskSlashdot` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Developers Feed](actions/get-developers-feed.md) | `GET slashdotDevelopers` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Games Feed](actions/get-games-feed.md) | `GET slashdotGames` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Linux Feed](actions/get-linux-feed.md) | `GET slashdotLinux` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Main Feed](actions/get-main-feed.md) | `GET slashdotMain` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Politics Feed](actions/get-politics-feed.md) | `GET slashdotPolitics` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
| [Get Your Rights Online Feed](actions/get-your-rights-online-feed.md) | `GET slashdotYourRightsOnline` | [docs](https://news.slashdot.org/faq/feeds.shtml) |
