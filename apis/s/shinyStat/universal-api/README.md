# <img src="https://images.mindcloud.co/apps/icons/id8-spb-inn-1775588093824_1775588151418.png" alt="ShinyStat logo" width="28" height="28"> ShinyStat: Universal API

Analyze traffic, conversions, and visitor behavior

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shinyStat/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shinystat.com
- **Vendor API docs:** https://www.shinystat.com/en/guida.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Sign In](actions/sign-in.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shinyStat/latest/actions/sign-in?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Countryvisit

| Action | Method | Description |
| --- | --- | --- |
| [List Country Visits](actions/list-country-visits.md) | GET |  |

### Landingpage

| Action | Method | Description |
| --- | --- | --- |
| [List Landing Pages](actions/list-landing-pages.md) | GET | Retrieves landing page metrics from ShinyStat. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Sign In](actions/sign-in.md) | GET | Retrieves an authenticated session from ShinyStat. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Bounce Rate](actions/get-bounce-rate.md) | GET | Retrieves the bounce rate from ShinyStat. |
| [Get Summary Dashboard](actions/get-summary-dashboard.md) | GET | Retrieves the summary dashboard from ShinyStat. |
| [Get Time On Site](actions/get-time-on-site.md) | GET | Retrieves time on site metrics from ShinyStat. |
| [List Average Time On Pages](actions/list-average-time-on-pages.md) | GET | Retrieves average time on page metrics from ShinyStat. |
| [List Bounce Visits](actions/list-bounce-visits.md) | GET | Retrieves bounce visit metrics from ShinyStat. |
| [List Daily Unique Visitors](actions/list-daily-unique-visitors.md) | GET | Retrieves daily unique visitor metrics from ShinyStat. |
| [List Latest Visits (100/200/500)](actions/list-latest-visits100200500.md) | GET | Retrieves the latest 100, 200, or 500 visits from ShinyStat. |
| [List Latest 15 Visits](actions/list-latest15-visits.md) | GET | Retrieves the latest 15 visits from ShinyStat. |
| [List Monthly Unique Visitors](actions/list-monthly-unique-visitors.md) | GET | Retrieves monthly unique visitor metrics from ShinyStat. |
| [List New Visitors](actions/list-new-visitors.md) | GET | Retrieves new visitor metrics from ShinyStat. |
| [List New Vs Returning Visitors](actions/list-new-vs-returning-visitors.md) | GET | Retrieves new versus returning visitor metrics from ShinyStat. |
| [List Page Views](actions/list-page-views.md) | GET | Retrieves page view report data from ShinyStat. |
| [List Page Views Per Visit](actions/list-page-views-per-visit.md) | GET | Retrieves page views per visit from ShinyStat. |
| [List Requests Per Page](actions/list-requests-per-page.md) | GET | Retrieves requests per page from ShinyStat. |
| [List Time On Each Page](actions/list-time-on-each-page.md) | GET | Retrieves time on page metrics for each page from ShinyStat. |
| [List Visit Frequency](actions/list-visit-frequency.md) | GET | Retrieves visit frequency metrics from ShinyStat. |
| [List Visits](actions/list-visits.md) | GET | Retrieves visit report data from ShinyStat. |
| [List Visits By Hour](actions/list-visits-by-hour.md) | GET | Retrieves hourly visit metrics from ShinyStat. |
| [List Visits By Week](actions/list-visits-by-week.md) | GET | Retrieves weekly visit metrics from ShinyStat. |
| [List Weekly Unique Visitors](actions/list-weekly-unique-visitors.md) | GET | Retrieves weekly unique visitor metrics from ShinyStat. |

