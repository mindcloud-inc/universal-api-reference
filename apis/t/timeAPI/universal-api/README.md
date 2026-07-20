# <img src="https://images.mindcloud.co/apps/icons/time-api_1777993522164.png" alt="TimeAPI logo" width="28" height="28"> TimeAPI: Universal API

TimeAPI provides public REST endpoints for current time, Unix timestamps, and IANA timezone lookup data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeAPI/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.timeapi.io
- **Vendor API docs:** https://www.timeapi.io/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current UTC Time](actions/get-current-utc-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeAPI/latest/actions/get-current-utc-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Current Time By Coordinates

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Time By Coordinates](actions/get-current-time-by-coordinates.md) | GET | Retrieves the current time by coordinates from TimeAPI. |

### Current Time By Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Time By IP Address](actions/get-current-time-by-ip-address.md) | GET | Retrieves the current time by IP address from TimeAPI. |

### Current Time By Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Time By Time Zone](actions/get-current-time-by-time-zone.md) | GET | Retrieves the current time for an IANA time zone from TimeAPI. |

### Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Available Time Zones](actions/list-available-time-zones.md) | GET | Retrieves available IANA time zones from TimeAPI. |

### Time Zone Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Zone Details](actions/get-time-zone-details.md) | GET | Retrieves time zone details by IANA name from TimeAPI. |

### Time Zone Details By Coordinates

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Zone Details By Coordinates](actions/get-time-zone-details-by-coordinates.md) | GET | Retrieves time zone details by coordinates from TimeAPI. |

### Unix Timestamp

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Unix Timestamp](actions/get-current-unix-timestamp.md) | GET | Retrieves the current Unix timestamp from TimeAPI. |

### Unix Timestamp Microseconds

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Unix Timestamp Microseconds](actions/get-current-unix-timestamp-microseconds.md) | GET | Retrieves the current Unix timestamp in microseconds from TimeAPI. |

### Unix Timestamp Milliseconds

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Unix Timestamp Milliseconds](actions/get-current-unix-timestamp-milliseconds.md) | GET | Retrieves the current Unix timestamp in milliseconds from TimeAPI. |

### Unix Timestamp Nanoseconds

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Unix Timestamp Nanoseconds](actions/get-current-unix-timestamp-nanoseconds.md) | GET | Retrieves the current Unix timestamp in nanoseconds from TimeAPI. |

### Utc Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Current UTC Time](actions/get-current-utc-time.md) | GET | Retrieves the current UTC time from TimeAPI. |

