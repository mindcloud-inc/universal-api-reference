# <img src="https://images.mindcloud.co/apps/icons/favicon-www-digitraffic-fi-48x48_1777483318857.png" alt="Finnish Railway Traffic logo" width="28" height="28"> Finnish Railway Traffic: Universal API

Open railway traffic data for Finland from Fintraffic's Digitraffic service, including live trains, timetables, train locations, passenger information messages, route sets, compositions, track work and traffic restriction notifications, and railway metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finnishRailwayTraffic/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digitraffic.fi/en/railway-traffic/
- **Vendor API docs:** https://www.digitraffic.fi/en/railway-traffic/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get latest train by number](actions/get-latest-train-by-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/get-latest-train-by-number?connectionId=$CONNECTION_ID&trainNumber=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Cause Category Code

| Action | Method | Description |
| --- | --- | --- |
| [List cause category codes](actions/list-cause-category-codes.md) | GET | Retrieves cause category codes from Finnish Railway Traffic. |

### Detailed Cause Category Code

| Action | Method | Description |
| --- | --- | --- |
| [List detailed cause category codes](actions/list-detailed-cause-category-codes.md) | GET | Retrieves detailed cause category codes from Finnish Railway Traffic. |

### Live Train

| Action | Method | Description |
| --- | --- | --- |
| [List live trains](actions/list-live-trains.md) | GET | Retrieves live trains from Finnish Railway Traffic. |
| [List live trains by station](actions/list-live-trains-by-station.md) | GET | Retrieves live trains for a station from Finnish Railway Traffic. |
| [Search live trains between stations](actions/search-live-trains-between-stations.md) | GET | Finds live trains between stations in Finnish Railway Traffic. |

### Passenger Information Message

| Action | Method | Description |
| --- | --- | --- |
| [List active passenger information messages](actions/list-active-passenger-information-messages.md) | GET | Retrieves active passenger information messages from Finnish Railway Traffic. |
| [List passenger information messages updated after date](actions/list-passenger-information-messages-updated-after-date.md) | GET | Retrieves passenger information messages updated after a date in Finnish Railway Traffic. |

### Railway Operator

| Action | Method | Description |
| --- | --- | --- |
| [List operators](actions/list-operators.md) | GET | Retrieves operators from Finnish Railway Traffic. |

### Railway Station

| Action | Method | Description |
| --- | --- | --- |
| [List stations](actions/list-stations.md) | GET | Retrieves stations from Finnish Railway Traffic. |

### Railway Station Geojson

| Action | Method | Description |
| --- | --- | --- |
| [List stations as GeoJSON](actions/list-stations-as-geojson.md) | GET | Retrieves stations as GeoJSON from Finnish Railway Traffic. |

### Routeset

| Action | Method | Description |
| --- | --- | --- |
| [List routesets updated after version](actions/list-routesets-updated-after-version.md) | GET | Retrieves routesets updated after a version in Finnish Railway Traffic. |

### Third Cause Category Code

| Action | Method | Description |
| --- | --- | --- |
| [List third cause category codes](actions/list-third-cause-category-codes.md) | GET | Retrieves third cause category codes from Finnish Railway Traffic. |

### Timetable Period

| Action | Method | Description |
| --- | --- | --- |
| [List timetable periods](actions/list-timetable-periods.md) | GET | Retrieves timetable periods from Finnish Railway Traffic. |

### Track Section

| Action | Method | Description |
| --- | --- | --- |
| [List track sections](actions/list-track-sections.md) | GET | Retrieves track sections from Finnish Railway Traffic. |

### Trackwork Notification

| Action | Method | Description |
| --- | --- | --- |
| [List trackwork notifications](actions/list-trackwork-notifications.md) | GET | Retrieves trackwork notifications in JSON from Finnish Railway Traffic. |

### Trackwork Notification Geojson

| Action | Method | Description |
| --- | --- | --- |
| [List trackwork notifications as GeoJSON](actions/list-trackwork-notifications-as-geojson.md) | GET | Retrieves trackwork notifications as GeoJSON from Finnish Railway Traffic. |

### Trackwork Notification Status

| Action | Method | Description |
| --- | --- | --- |
| [List trackwork notification status](actions/list-trackwork-notification-status.md) | GET | Retrieves trackwork notification versions from Finnish Railway Traffic. |

### Traffic Restriction Notification

| Action | Method | Description |
| --- | --- | --- |
| [List traffic restriction notifications](actions/list-traffic-restriction-notifications.md) | GET | Retrieves traffic restriction notifications in JSON from Finnish Railway Traffic. |

### Traffic Restriction Notification Geojson

| Action | Method | Description |
| --- | --- | --- |
| [List traffic restriction notifications as GeoJSON](actions/list-traffic-restriction-notifications-as-geojson.md) | GET | Retrieves traffic restriction notifications as GeoJSON from Finnish Railway Traffic. |

### Traffic Restriction Notification Status

| Action | Method | Description |
| --- | --- | --- |
| [List traffic restriction notification status](actions/list-traffic-restriction-notification-status.md) | GET | Retrieves traffic restriction notification versions from Finnish Railway Traffic. |

### Train

| Action | Method | Description |
| --- | --- | --- |
| [Get latest train by number](actions/get-latest-train-by-number.md) | GET | Retrieves the latest train by number from Finnish Railway Traffic. |
| [List trains by departure date](actions/list-trains-by-departure-date.md) | GET | Retrieves trains by departure date from Finnish Railway Traffic. |
| [List trains updated after version](actions/list-trains-updated-after-version.md) | GET | Retrieves trains updated after a version in Finnish Railway Traffic. |

### Train Category

| Action | Method | Description |
| --- | --- | --- |
| [List train categories](actions/list-train-categories.md) | GET | Retrieves train categories from Finnish Railway Traffic. |

### Train Composition

| Action | Method | Description |
| --- | --- | --- |
| [List compositions by departure date](actions/list-compositions-by-departure-date.md) | GET | Retrieves train compositions by departure date from Finnish Railway Traffic. |
| [List compositions updated after version](actions/list-compositions-updated-after-version.md) | GET | Retrieves compositions updated after a version in Finnish Railway Traffic. |

### Train Location

| Action | Method | Description |
| --- | --- | --- |
| [List latest train locations](actions/list-latest-train-locations.md) | GET | Retrieves latest train locations from Finnish Railway Traffic. |

### Train Location Geojson

| Action | Method | Description |
| --- | --- | --- |
| [List latest train locations as GeoJSON](actions/list-latest-train-locations-as-geojson.md) | GET | Retrieves latest train locations as GeoJSON from Finnish Railway Traffic. |

### Train Running Message

| Action | Method | Description |
| --- | --- | --- |
| [List train tracking messages updated after version](actions/list-train-tracking-messages-updated-after-version.md) | GET | Retrieves train tracking messages updated after a version in Finnish Railway Traffic. |

### Train Running Message Rule

| Action | Method | Description |
| --- | --- | --- |
| [List train running message rules](actions/list-train-running-message-rules.md) | GET | Retrieves train running message rules from Finnish Railway Traffic. |

### Train Type

| Action | Method | Description |
| --- | --- | --- |
| [List train types](actions/list-train-types.md) | GET | Retrieves train types from Finnish Railway Traffic. |

