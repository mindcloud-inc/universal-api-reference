# <img src="https://images.mindcloud.co/apps/icons/slashdot_1776449351709.png" alt="Slashdot logo" width="28" height="28"> Slashdot: Universal API

Public RSS feeds for Slashdot stories and sections.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/slashdot/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://slashdot.org/
- **Vendor API docs:** https://news.slashdot.org/faq/feeds.shtml

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Main Feed](actions/get-main-feed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-main-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Feed Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Ask Slashdot Feed](actions/get-ask-slashdot-feed.md) | GET | Retrieves the Ask Slashdot feed. |
| [Get Developers Feed](actions/get-developers-feed.md) | GET | Retrieves the Developers feed from Slashdot. |
| [Get Games Feed](actions/get-games-feed.md) | GET | Retrieves the Games feed from Slashdot. |
| [Get Linux Feed](actions/get-linux-feed.md) | GET | Retrieves the Linux feed from Slashdot. |
| [Get Main Feed](actions/get-main-feed.md) | GET | Retrieves the main feed from Slashdot. |
| [Get Politics Feed](actions/get-politics-feed.md) | GET | Retrieves the Politics feed from Slashdot. |
| [Get Your Rights Online Feed](actions/get-your-rights-online-feed.md) | GET | Retrieves the Your Rights Online feed from Slashdot. |

