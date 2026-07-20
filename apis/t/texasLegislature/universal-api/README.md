# <img src="https://images.mindcloud.co/apps/icons/texas-legislature_1776436167065.png" alt="Texas Legislature logo" width="28" height="28"> Texas Legislature: Universal API

Access public Texas Legislature Online legislative activity RSS feeds and official TLC bulk-file guidance for bill text, analyses, fiscal notes, reports, witness lists, and bill history XML.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/texasLegislature/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://capitol.texas.gov/
- **Vendor API docs:** https://capitol.texas.gov/billlookup/filedownloads.aspx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Today's Bill Analyses RSS Feed](actions/get-todays-bill-analyses-rss-feed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/texasLegislature/latest/actions/get-todays-bill-analyses-rss-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Bill Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Today's Bill Analyses RSS Feed](actions/get-todays-bill-analyses-rss-feed.md) | GET | Retrieves today's bill analyses from Texas Legislature. |

### Bill Text

| Action | Method | Description |
| --- | --- | --- |
| [Get Today's Bill Text RSS Feed](actions/get-todays-bill-text-rss-feed.md) | GET | Retrieves today's bill text from Texas Legislature. |

### Committee Meeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Upcoming House Committee Meetings RSS Feed](actions/get-upcoming-house-committee-meetings-rss-feed.md) | GET | Retrieves upcoming House committee meetings from Texas Legislature. |
| [Get Upcoming Senate Committee Meetings RSS Feed](actions/get-upcoming-senate-committee-meetings-rss-feed.md) | GET | Retrieves upcoming Senate committee meetings from Texas Legislature. |

### Filed Bill

| Action | Method | Description |
| --- | --- | --- |
| [Get Today's House Filed Bills RSS Feed](actions/get-todays-house-filed-bills-rss-feed.md) | GET | Retrieves today's House-filed bills from Texas Legislature. |
| [Get Today's Senate Filed Bills RSS Feed](actions/get-todays-senate-filed-bills-rss-feed.md) | GET | Retrieves today's Senate-filed bills from Texas Legislature. |

### Fiscal Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Today's Fiscal Notes RSS Feed](actions/get-todays-fiscal-notes-rss-feed.md) | GET | Retrieves today's fiscal notes from Texas Legislature. |

### Legislative Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Upcoming House Calendars RSS Feed](actions/get-upcoming-house-calendars-rss-feed.md) | GET | Retrieves upcoming House calendars from Texas Legislature. |
| [Get Upcoming Senate Calendars RSS Feed](actions/get-upcoming-senate-calendars-rss-feed.md) | GET | Retrieves upcoming Senate calendars from Texas Legislature. |

### Passed Bill

| Action | Method | Description |
| --- | --- | --- |
| [Get Today's Passed Bills RSS Feed](actions/get-todays-passed-bills-rss-feed.md) | GET | Retrieves today's passed bills from Texas Legislature. |

