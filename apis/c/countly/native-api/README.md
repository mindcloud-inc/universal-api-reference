# Countly: Native API Reference

A consolidated summary of Countly's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.count.ly/reference/rest-api-reference
- **API base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`

## Authentication

### API Key

Authenticate with a Countly user API key. Countly REST endpoints expect the key as the api_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.count.ly/reference/api-key)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Analytics Countries](actions/get-analytics-countries.md) | `GET /o/analytics/countries` | [docs](https://api.count.ly/reference/oanalyticscountries) |
| [Get Analytics Dashboard](actions/get-analytics-dashboard.md) | `GET /o/analytics/dashboard` | [docs](https://api.count.ly/reference/oanalyticsdashboard) |
| [Get Analytics Events](actions/get-analytics-events.md) | `GET /o/analytics/events` | [docs](https://api.count.ly/reference/oanalyticsevents) |
| [Get Analytics Metric](actions/get-analytics-metric.md) | `GET /o/analytics/metric` | [docs](https://api.count.ly/reference/oanalyticsmetric) |
| [Get Analytics Sessions](actions/get-analytics-sessions.md) | `GET /o/analytics/sessions` | [docs](https://api.count.ly/reference/oanalyticssessions) |
| [Get App Details](actions/get-app-details.md) | `GET /o/apps/details` | [docs](https://api.count.ly/reference/oappsdetails) |
| [Get App Versions Analytics](actions/get-app-versions-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodapp_versions) |
| [Get Campaign Data](actions/get-campaign-data.md) | `GET /o/campaign` | [docs](https://api.count.ly/reference/ocampaigndata) |
| [Get Carriers Analytics](actions/get-carriers-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodcarriers) |
| [Get Cities Analytics](actions/get-cities-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodcities) |
| [Get Current User](actions/get-current-user.md) | `GET /o/users/me` | [docs](https://api.count.ly/reference/ousersmeapi_keyapi_key) |
| [Get Device Details Analytics](actions/get-device-details-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethoddevice_details) |
| [Get Devices Analytics](actions/get-devices-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethoddevices) |
| [Get Duration Analytics](actions/get-duration-analytics.md) | `GET /o/analytics/durations` | [docs](https://api.count.ly/reference/oanalyticsdurations) |
| [Get Event Analytics](actions/get-event-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodevents) |
| [Get Frequency Analytics](actions/get-frequency-analytics.md) | `GET /o/analytics/frequency` | [docs](https://api.count.ly/reference/oanalyticsfrequency) |
| [Get Funnel Analytics](actions/get-funnel-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodfunnel) |
| [Get Large Segmentation Metadata](actions/get-large-segmentation-metadata.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodsegmentation_big_meta) |
| [Get Live Analytics](actions/get-live-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodlive) |
| [Get Live Graph](actions/get-live-graph.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodlive_graph) |
| [Get Locations Analytics](actions/get-locations-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodlocations) |
| [Get Loyalty Analytics](actions/get-loyalty-analytics.md) | `GET /o/analytics/loyalty` | [docs](https://api.count.ly/reference/oanalyticsloyalty) |
| [Get Period Object](actions/get-period-object.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodget_period_obj) |
| [Get Segmentation](actions/get-segmentation.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodsegmentation) |
| [Get Segmentation Metadata](actions/get-segmentation-metadata.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodsegmentation_meta) |
| [Get Sessions Analytics](actions/get-sessions-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodsessions) |
| [Get Total Users Metric](actions/get-total-users-metric.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodtotal_users) |
| [Get User Details](actions/get-user-details.md) | `GET /o` | [docs](https://api.count.ly/reference/omethoduser_detailsuid) |
| [Get Users Analytics](actions/get-users-analytics.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodusers) |
| [List Apps](actions/list-apps.md) | `GET /o/apps/all` | [docs](https://api.count.ly/reference/oappsall) |
| [List Campaigns](actions/list-campaigns.md) | `GET /o/campaign` | [docs](https://api.count.ly/reference/ocampaign) |
| [List Drill Bookmarks](actions/list-drill-bookmarks.md) | `GET /o` | [docs](https://api.count.ly/reference/omethoddrill_bookmarks) |
| [List Events](actions/list-events.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodget_events) |
| [List Funnels](actions/list-funnels.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodget_funnels) |
| [List Geolocations](actions/list-geolocations.md) | `GET /o` | [docs](https://api.count.ly/reference/omethodget_locations) |
| [List My Apps](actions/list-my-apps.md) | `GET /o/apps/mine` | [docs](https://api.count.ly/reference/oappsmine) |
| [List Push Messages](actions/list-push-messages.md) | `GET /o/pushes/all` | [docs](https://api.count.ly/reference/opushes) |
| [List User Profiles](actions/list-user-profiles.md) | `GET /o` | [docs](https://api.count.ly/reference/omethoduser_details) |
| [List Users](actions/list-users.md) | `GET /o/users/all` | [docs](https://api.count.ly/reference/ousersall) |
| [Ping Server](actions/ping-server.md) | `GET /o/ping` | [docs](https://api.count.ly/reference/oping) |
