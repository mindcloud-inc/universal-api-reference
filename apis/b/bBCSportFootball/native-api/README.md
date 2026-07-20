# BBC Sport - Football: Native API Reference

A consolidated summary of BBC Sport - Football's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://support.bbc.co.uk/platform/feeds/SportFeeds.htm
- **API base URL:** `http://newsrss.bbc.co.uk/rss/sportonline_uk_edition`

## Authentication

### No Authentication

Public BBC Sport football RSS feed with no credentials required.

This API does not require request authentication.

[Official authentication documentation](https://support.bbc.co.uk/platform/feeds/SportFeeds.htm)

## API conventions

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Football Africa Articles](actions/list-football-africa-articles.md) | `GET /football/africa/rss.xml` |  |
| [List Football Articles](actions/list-football-articles.md) | `GET /football/rss.xml` | [docs](https://support.bbc.co.uk/platform/feeds/SportFeeds.htm) |
| [List Football Championship Articles](actions/list-football-championship-articles.md) | `GET /football/eng_div_1/rss.xml` |  |
| [List Football Europe Articles](actions/list-football-europe-articles.md) | `GET /football/europe/rss.xml` |  |
| [List Football FA Cup Articles](actions/list-football-fa-cup-articles.md) | `GET /football/fa_cup/rss.xml` |  |
| [List Football Final Score Articles](actions/list-football-final-score-articles.md) | `GET /football/score_on_bbci/rss.xml` |  |
| [List Football Focus Articles](actions/list-football-focus-articles.md) | `GET /football/football_focus/rss.xml` |  |
| [List Football Gossip Articles](actions/list-football-gossip-articles.md) | `GET /football/gossip_and_transfers/rss.xml` |  |
| [List Football Internationals Articles](actions/list-football-internationals-articles.md) | `GET /football/internationals/rss.xml` |  |
| [List Football Irish Articles](actions/list-football-irish-articles.md) | `GET /football/irish/rss.xml` |  |
| [List Football League One Articles](actions/list-football-league-one-articles.md) | `GET /football/eng_div_2/rss.xml` |  |
| [List Football League Two Articles](actions/list-football-league-two-articles.md) | `GET /football/eng_div_3/rss.xml` |  |
| [List Football Match of the Day Articles](actions/list-football-match-of-the-day-articles.md) | `GET /football/match_of_the_day/rss.xml` |  |
| [List Football My Club Articles](actions/list-football-my-club-articles.md) | `GET /football/teams/rss.xml` |  |
| [List Football Non League Articles](actions/list-football-non-league-articles.md) | `GET /football/eng_conf/rss.xml` |  |
| [List Football Premier League Articles](actions/list-football-premier-league-articles.md) | `GET /football/eng_prem/rss.xml` |  |
| [List Football Scottish Cups Articles](actions/list-football-scottish-cups-articles.md) | `GET /football/scot_cups/rss.xml` |  |
| [List Football Scottish League Articles](actions/list-football-scottish-league-articles.md) | `GET /football/scot_div_1/rss.xml` |  |
| [List Football Scottish Premier Articles](actions/list-football-scottish-premier-articles.md) | `GET /football/scot_prem/rss.xml` |  |
| [List Football Welsh Articles](actions/list-football-welsh-articles.md) | `GET /football/league_of_wales/rss.xml` |  |
