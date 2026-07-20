# <img src="https://images.mindcloud.co/apps/icons/b-bcsport-football_1776361623614.png" alt="BBC Sport - Football logo" width="28" height="28"> BBC Sport - Football: Universal API

Browse BBC Sport football headlines and article feeds

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bBCSportFootball/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bbc.co.uk/sport/football
- **Vendor API docs:** https://support.bbc.co.uk/platform/feeds/SportFeeds.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Football Africa Articles](actions/list-football-africa-articles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportFootball/latest/actions/list-football-africa-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Football Africa Articles](actions/list-football-africa-articles.md) | GET |  |
| [List Football Articles](actions/list-football-articles.md) | GET |  |
| [List Football Championship Articles](actions/list-football-championship-articles.md) | GET |  |
| [List Football Europe Articles](actions/list-football-europe-articles.md) | GET |  |
| [List Football FA Cup Articles](actions/list-football-fa-cup-articles.md) | GET |  |
| [List Football Final Score Articles](actions/list-football-final-score-articles.md) | GET |  |
| [List Football Focus Articles](actions/list-football-focus-articles.md) | GET |  |
| [List Football Gossip Articles](actions/list-football-gossip-articles.md) | GET |  |
| [List Football Internationals Articles](actions/list-football-internationals-articles.md) | GET |  |
| [List Football Irish Articles](actions/list-football-irish-articles.md) | GET |  |
| [List Football League One Articles](actions/list-football-league-one-articles.md) | GET |  |
| [List Football League Two Articles](actions/list-football-league-two-articles.md) | GET |  |
| [List Football Match of the Day Articles](actions/list-football-match-of-the-day-articles.md) | GET |  |
| [List Football My Club Articles](actions/list-football-my-club-articles.md) | GET |  |
| [List Football Non League Articles](actions/list-football-non-league-articles.md) | GET |  |
| [List Football Premier League Articles](actions/list-football-premier-league-articles.md) | GET |  |
| [List Football Scottish Cups Articles](actions/list-football-scottish-cups-articles.md) | GET |  |
| [List Football Scottish League Articles](actions/list-football-scottish-league-articles.md) | GET |  |
| [List Football Scottish Premier Articles](actions/list-football-scottish-premier-articles.md) | GET |  |
| [List Football Welsh Articles](actions/list-football-welsh-articles.md) | GET |  |

