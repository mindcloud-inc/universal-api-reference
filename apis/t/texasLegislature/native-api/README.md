# Texas Legislature: Native API Reference

A consolidated summary of Texas Legislature's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://capitol.texas.gov/billlookup/filedownloads.aspx
- **API base URL:** `https://capitol.texas.gov`

## Authentication

### No Authentication

Public Texas Legislature Online RSS feeds and anonymous FTP file downloads require no credentials.

This API does not require request authentication.

[Official authentication documentation](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Today's Bill Analyses RSS Feed](actions/get-todays-bill-analyses-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysbillanalyses` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Today's Bill Text RSS Feed](actions/get-todays-bill-text-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysbilltext` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Today's Fiscal Notes RSS Feed](actions/get-todays-fiscal-notes-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysfiscalnotes` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Today's House Filed Bills RSS Feed](actions/get-todays-house-filed-bills-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysfiledhouse` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Today's Passed Bills RSS Feed](actions/get-todays-passed-bills-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysbillspassed` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Today's Senate Filed Bills RSS Feed](actions/get-todays-senate-filed-bills-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=todaysfiledsenate` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Upcoming House Calendars RSS Feed](actions/get-upcoming-house-calendars-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=upcomingcalendarshouse` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Upcoming House Committee Meetings RSS Feed](actions/get-upcoming-house-committee-meetings-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=upcomingmeetingshouse` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Upcoming Senate Calendars RSS Feed](actions/get-upcoming-senate-calendars-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=upcomingcalendarssenate` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
| [Get Upcoming Senate Committee Meetings RSS Feed](actions/get-upcoming-senate-committee-meetings-rss-feed.md) | `GET /MyTLO/RSS/RSS.aspx?Type=upcomingmeetingssenate` | [docs](https://capitol.texas.gov/MyTLO/RSS/rssFeeds.aspx) |
