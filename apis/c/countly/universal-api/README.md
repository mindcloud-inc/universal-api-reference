# <img src="https://images.mindcloud.co/apps/icons/countly-logo_1776183491281.jpeg" alt="Countly logo" width="28" height="28"> Countly: Universal API

Countly is a product analytics and customer experience platform for querying apps, users, events, dashboards, funnels, campaigns, and operational analytics through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/countly/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://count.ly
- **Vendor API docs:** https://api.count.ly/reference/rest-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Analytics Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Dashboard](actions/get-analytics-dashboard.md) | GET | Retrieves the analytics dashboard from Countly. |

### Analytics Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Events](actions/get-analytics-events.md) | GET | Retrieves all analytics events from Countly. |

### Analytics Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Metric](actions/get-analytics-metric.md) | GET | Retrieves an analytics metric from Countly. |

### App Version Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get App Versions Analytics](actions/get-app-versions-analytics.md) | GET | Retrieves app version analytics from Countly. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get App Details](actions/get-app-details.md) | GET | Retrieves application details from Countly. |
| [List Apps](actions/list-apps.md) | GET | Retrieves all apps from Countly. |
| [List My Apps](actions/list-my-apps.md) | GET | Retrieves the current user's apps from Countly. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all campaigns from Countly. |

### Campaign Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Data](actions/get-campaign-data.md) | GET | Retrieves all campaign data from Countly. |

### Carrier Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Carriers Analytics](actions/get-carriers-analytics.md) | GET | Retrieves all carrier analytics from Countly. |

### City Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Cities Analytics](actions/get-cities-analytics.md) | GET | Retrieves all city analytics from Countly. |

### Country Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Countries](actions/get-analytics-countries.md) | GET | Retrieves all country analytics from Countly. |

### Device Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Devices Analytics](actions/get-devices-analytics.md) | GET | Retrieves all device analytics from Countly. |

### Device Detail Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Details Analytics](actions/get-device-details-analytics.md) | GET | Retrieves device detail analytics from Countly. |

### Drill Bookmark

| Action | Method | Description |
| --- | --- | --- |
| [List Drill Bookmarks](actions/list-drill-bookmarks.md) | GET | Retrieves all drill bookmarks from Countly. |

### Duration Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Duration Analytics](actions/get-duration-analytics.md) | GET | Retrieves all duration analytics from Countly. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves all events from Countly. |

### Event Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Analytics](actions/get-event-analytics.md) | GET | Retrieves all event analytics from Countly. |

### Frequency Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Frequency Analytics](actions/get-frequency-analytics.md) | GET | Retrieves all frequency analytics from Countly. |

### Funnel

| Action | Method | Description |
| --- | --- | --- |
| [List Funnels](actions/list-funnels.md) | GET | Retrieves all funnels from Countly. |

### Funnel Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Funnel Analytics](actions/get-funnel-analytics.md) | GET | Retrieves all funnel analytics from Countly. |

### Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [List Geolocations](actions/list-geolocations.md) | GET | Retrieves all geolocations from Countly. |

### Large Segmentation Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Large Segmentation Metadata](actions/get-large-segmentation-metadata.md) | GET | Retrieves large segmentation metadata from Countly. |

### Live Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Analytics](actions/get-live-analytics.md) | GET | Retrieves all live analytics from Countly. |

### Live Graph

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Graph](actions/get-live-graph.md) | GET | Retrieves the live graph from Countly. |

### Location Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Locations Analytics](actions/get-locations-analytics.md) | GET | Retrieves all location analytics from Countly. |

### Loyalty Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Loyalty Analytics](actions/get-loyalty-analytics.md) | GET | Retrieves all loyalty analytics from Countly. |

### Period Object

| Action | Method | Description |
| --- | --- | --- |
| [Get Period Object](actions/get-period-object.md) | GET | Retrieves the period object from Countly. |

### Push Message

| Action | Method | Description |
| --- | --- | --- |
| [List Push Messages](actions/list-push-messages.md) | GET | Retrieves all push messages from Countly. |

### Segmentation

| Action | Method | Description |
| --- | --- | --- |
| [Get Segmentation](actions/get-segmentation.md) | GET | Retrieves all segmentation data from Countly. |

### Segmentation Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Segmentation Metadata](actions/get-segmentation-metadata.md) | GET | Retrieves all segmentation metadata from Countly. |

### Server Status

| Action | Method | Description |
| --- | --- | --- |
| [Ping Server](actions/ping-server.md) | GET | Retrieves the server status from Countly. |

### Session Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics Sessions](actions/get-analytics-sessions.md) | GET | Retrieves all analytics sessions from Countly. |
| [Get Sessions Analytics](actions/get-sessions-analytics.md) | GET | Retrieves all session analytics from Countly. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Countly. |
| [List Users](actions/list-users.md) | GET | Retrieves all users from Countly. |

### User Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Users Analytics](actions/get-users-analytics.md) | GET | Retrieves all user analytics from Countly. |

### User Details

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves all user details from Countly. |

### User Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Total Users Metric](actions/get-total-users-metric.md) | GET | Retrieves the total users metric from Countly. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [List User Profiles](actions/list-user-profiles.md) | GET | Retrieves all user profiles from Countly. |

