# <img src="https://images.mindcloud.co/apps/icons/bkk-icon_1777496277791.png" alt="BKK Futar logo" width="28" height="28"> BKK Futar: Universal API

Access planned and real-time public transportation data from BKK Futar for Budapest, including stops, arrivals, departures, schedules, vehicles, alerts, references, and bicycle rental stations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bKKFutar/latest
- **Category:** Support / Field Service
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opendata.bkk.hu/data-sources
- **Vendor API docs:** https://bkkfutar.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bicycle Rental Stations](actions/get-bicycle-rental-stations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Alert Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Alerts](actions/search-alerts.md) | GET | Finds active alerts in BKK Futar by search criteria. |

### Bicycle Rental Station

| Action | Method | Description |
| --- | --- | --- |
| [Get Bicycle Rental Stations](actions/get-bicycle-rental-stations.md) | GET | Retrieves bicycle rental stations from BKK Futar. |

### Reference

| Action | Method | Description |
| --- | --- | --- |
| [Get References](actions/get-references.md) | GET | Retrieves ID-based references from BKK Futar. |

### Stop

| Action | Method | Description |
| --- | --- | --- |
| [Get Stops For Location](actions/get-stops-for-location.md) | GET | Retrieves stops for a selected location, or all stops, in BKK Futar. |

### Stop Arrival And Departure

| Action | Method | Description |
| --- | --- | --- |
| [Get Arrivals And Departures For Stop](actions/get-arrivals-and-departures-for-stop.md) | GET | Retrieves arrivals and departures for a BKK Futar stop. |

### Stop Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule For Stop](actions/get-schedule-for-stop.md) | GET | Retrieves the schedule for a selected BKK Futar stop. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicles For Stop](actions/get-vehicles-for-stop.md) | GET | Retrieves vehicles on routes containing a selected BKK Futar stop. |

