# Golemio API Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Golemio API expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-air-quality-station-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Golemio API actions that support pagination

- [List Air Quality Station History](actions/list-air-quality-station-history.md)
- [List Air Quality Stations](actions/list-air-quality-stations.md)
- [List Bicycle Counters](actions/list-bicycle-counters.md)
- [List City Districts](actions/list-city-districts.md)
- [List Gardens](actions/list-gardens.md)
- [List Medical Institutions](actions/list-medical-institutions.md)
- [List Municipal Authorities](actions/list-municipal-authorities.md)
- [List Municipal Libraries](actions/list-municipal-libraries.md)
- [List Municipal Police Stations](actions/list-municipal-police-stations.md)
- [List Parking Locations](actions/list-parking-locations.md)
- [List Parking Machines](actions/list-parking-machines.md)
- [List Parking Measurements](actions/list-parking-measurements.md)
- [List Parking Tariffs](actions/list-parking-tariffs.md)
- [List Waste Collection Stations](actions/list-waste-collection-stations.md)
