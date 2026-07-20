# <img src="https://images.mindcloud.co/apps/icons/postpone_1774019218902.png" alt="Postpone logo" width="28" height="28"> Postpone: Universal API

Schedule posts, manage tags, and track social media analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postpone/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postpone.app
- **Vendor API docs:** https://developers.postpone.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Aggregate Post Metrics](actions/get-aggregate-post-metrics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-aggregate-post-metrics?connectionId=$CONNECTION_ID&variables.startDate=string&variables.endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregate Post Metrics](actions/get-aggregate-post-metrics.md) | GET | Retrieves aggregate post metrics from Postpone. |
| [Get Aggregate Social Account Post Metrics](actions/get-aggregate-social-account-post-metrics.md) | GET | Retrieves aggregate social account post metrics from Postpone. |
| [Get Post Time Series Metrics](actions/get-post-time-series-metrics.md) | GET | Retrieves post time series metrics from Postpone. |
| [List Bluesky Submissions](actions/list-bluesky-submissions.md) | GET | Retrieves Bluesky submissions from Postpone. |
| [List Facebook Submissions](actions/list-facebook-submissions.md) | GET | Retrieves Facebook submissions from Postpone. |
| [List Instagram Submissions](actions/list-instagram-submissions.md) | GET | Retrieves Instagram submissions from Postpone. |
| [List LinkedIn Submissions](actions/list-linkedin-submissions.md) | GET | Retrieves LinkedIn submissions from Postpone. |
| [List Pinterest Submissions](actions/list-pinterest-submissions.md) | GET | Retrieves Pinterest submissions from Postpone. |
| [List Reddit Submissions](actions/list-reddit-submissions.md) | GET | Retrieves Reddit submissions from Postpone. |
| [List Threads Submissions](actions/list-threads-submissions.md) | GET | Retrieves Threads submissions from Postpone. |
| [List Twitter Submissions](actions/list-twitter-submissions.md) | GET | Retrieves X/Twitter submissions from Postpone. |
| [Schedule Bluesky Post](actions/schedule-bluesky-post.md) | POST | Schedules a Bluesky post in Postpone. |
| [Schedule Facebook Post](actions/schedule-facebook-post.md) | POST | Schedules a Facebook post in Postpone. |
| [Schedule Instagram Post](actions/schedule-instagram-post.md) | POST | Schedules an Instagram post in Postpone. |
| [Schedule LinkedIn Post](actions/schedule-linkedin-post.md) | POST | Schedules a LinkedIn post in Postpone. |
| [Schedule Pinterest Post](actions/schedule-pinterest-post.md) | POST | Schedules a Pinterest post in Postpone. |
| [Schedule Reddit Post](actions/schedule-reddit-post.md) | POST | Schedules a Reddit post in Postpone. |
| [Schedule Threads Post](actions/schedule-threads-post.md) | POST | Schedules a Threads post in Postpone. |
| [Schedule Tweet](actions/schedule-tweet.md) | POST | Schedules a tweet in Postpone. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [List Media](actions/list-media.md) | GET | Retrieves media from Postpone. |

### Post Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Post Tags](actions/list-post-tags.md) | GET | Retrieves post tags from Postpone. |

### Scheduled Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Next Schedule Dates](actions/list-next-schedule-dates.md) | GET | Retrieves next scheduled post dates from Postpone. |

### Social Account

| Action | Method | Description |
| --- | --- | --- |
| [List Social Accounts](actions/list-social-accounts.md) | GET | Retrieves social accounts from Postpone. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your profile from Postpone. |

