# <img src="https://images.mindcloud.co/apps/icons/chicago-transit-authority_1776427644284.png" alt="Chicago Transit Authority logo" width="28" height="28"> Chicago Transit Authority: Universal API

Chicago Transit Authority developer app for official CTA Train Tracker, route status, and detailed service alerts APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chicagoTransitAuthority/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.transitchicago.com/
- **Vendor API docs:** https://www.transitchicago.com/developers/default.aspx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Train Arrivals by Station](actions/get-train-arrivals-by-station.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chicagoTransitAuthority/latest/actions/get-train-arrivals-by-station?connectionId=$CONNECTION_ID&mapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Active Alerts](actions/list-active-alerts.md) | GET | Retrieves active alerts in Chicago Transit Authority. |
| [List Active Route Alerts](actions/list-active-route-alerts.md) | GET | Finds active alerts in Chicago Transit Authority by route ID. |
| [List Active Station Alerts](actions/list-active-station-alerts.md) | GET | Finds active alerts in Chicago Transit Authority by station ID. |
| [List Active Unplanned Alerts](actions/list-active-unplanned-alerts.md) | GET | Retrieves active unplanned alerts in Chicago Transit Authority. |
| [List Alerts by Route IDs](actions/list-alerts-by-route-ids.md) | GET | Finds alerts in Chicago Transit Authority by route ID. |
| [List Alerts by Start Date](actions/list-alerts-by-start-date.md) | GET | Finds alerts in Chicago Transit Authority by start date. |
| [List Alerts by Station IDs](actions/list-alerts-by-station-ids.md) | GET | Finds alerts in Chicago Transit Authority by station ID. |
| [List Detailed Alerts](actions/list-detailed-alerts.md) | GET | Retrieves detailed alerts in Chicago Transit Authority. |
| [List Non-Accessibility Alerts](actions/list-non-accessibility-alerts.md) | GET | Retrieves non-accessibility alerts in Chicago Transit Authority. |
| [List Planned Route Alerts](actions/list-planned-route-alerts.md) | GET | Finds planned alerts in Chicago Transit Authority by route ID. |
| [List Planned Station Alerts](actions/list-planned-station-alerts.md) | GET | Finds planned alerts in Chicago Transit Authority by station ID. |
| [List Recent Alerts](actions/list-recent-alerts.md) | GET | Retrieves recent alerts in Chicago Transit Authority. |
| [List Recent Route Alerts](actions/list-recent-route-alerts.md) | GET | Finds recent alerts in Chicago Transit Authority by route ID. |
| [List Recent Station Alerts](actions/list-recent-station-alerts.md) | GET | Finds recent alerts in Chicago Transit Authority by station ID. |
| [List Unplanned Alerts](actions/list-unplanned-alerts.md) | GET | Retrieves unplanned alerts in Chicago Transit Authority. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Train Arrivals by Platform Stop](actions/get-train-arrivals-by-platform-stop.md) | GET | Retrieves train arrival predictions in Chicago Transit Authority by platform stop. |
| [Get Train Arrivals by Platform Stop and Route](actions/get-train-arrivals-by-platform-stop-and-route.md) | GET | Retrieves train arrival predictions in Chicago Transit Authority by platform stop and route. |
| [Get Train Arrivals by Platform Stop Limit](actions/get-train-arrivals-by-platform-stop-limit.md) | GET | Retrieves limited train arrival predictions in Chicago Transit Authority by platform stop. |
| [Get Train Arrivals by Platform Stop Route Limit](actions/get-train-arrivals-by-platform-stop-route-limit.md) | GET | Retrieves limited train arrival predictions in Chicago Transit Authority by platform stop and route. |
| [Get Train Arrivals by Station](actions/get-train-arrivals-by-station.md) | GET | Retrieves train arrival predictions in Chicago Transit Authority by station. |
| [Get Train Arrivals by Station and Route](actions/get-train-arrivals-by-station-and-route.md) | GET | Retrieves train arrival predictions in Chicago Transit Authority by station and route. |
| [Get Train Arrivals by Station Limit](actions/get-train-arrivals-by-station-limit.md) | GET | Retrieves limited train arrival predictions in Chicago Transit Authority by station. |
| [Get Train Arrivals by Station Route Limit](actions/get-train-arrivals-by-station-route-limit.md) | GET | Retrieves limited train arrival predictions in Chicago Transit Authority by station and route. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Route Status by Route IDs](actions/get-route-status-by-route-ids.md) | GET | Finds route statuses in Chicago Transit Authority by route ID. |
| [Get Station Status by Station IDs](actions/get-station-status-by-station-ids.md) | GET | Finds station statuses in Chicago Transit Authority by station ID. |
| [List Bus Route Statuses](actions/list-bus-route-statuses.md) | GET | Retrieves bus route statuses in Chicago Transit Authority. |
| [List Rail Route Statuses](actions/list-rail-route-statuses.md) | GET | Retrieves rail route statuses in Chicago Transit Authority. |
| [List Route Statuses](actions/list-route-statuses.md) | GET | Retrieves route statuses in Chicago Transit Authority. |
| [List Station Statuses](actions/list-station-statuses.md) | GET | Retrieves station statuses in Chicago Transit Authority. |
| [List Systemwide Statuses](actions/list-systemwide-statuses.md) | GET | Retrieves systemwide statuses in Chicago Transit Authority. |

