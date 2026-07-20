# <img src="https://images.mindcloud.co/apps/icons/airlabs-icon_1777668648698.png" alt="Airlabs logo" width="28" height="28"> Airlabs: Universal API

Aviation data API for real-time flights, schedules, flight details, airports, airlines, routes, fleets, countries, time zones, tax codes, nearby airport lookup, and destination suggestions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airlabs/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://airlabs.co/
- **Vendor API docs:** https://airlabs.co/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping Airlabs](actions/ping-airlabs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/ping-airlabs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Aircraft

| Action | Method | Description |
| --- | --- | --- |
| [List Aircraft Fleets](actions/list-aircraft-fleets.md) | GET | Retrieves airline fleet data from Airlabs. |

### Airline

| Action | Method | Description |
| --- | --- | --- |
| [List Airlines](actions/list-airlines.md) | GET | Retrieves airline database records from Airlabs. |

### Airport

| Action | Method | Description |
| --- | --- | --- |
| [List Airports](actions/list-airports.md) | GET | Retrieves airport database records from Airlabs. |

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Ping Airlabs](actions/ping-airlabs.md) | GET | Retrieves API status details from Airlabs. |

### City

| Action | Method | Description |
| --- | --- | --- |
| [List Cities](actions/list-cities.md) | GET | Retrieves city database records from Airlabs. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves country database records from Airlabs. |

### Destination Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Destinations](actions/suggest-destinations.md) | GET | Finds destination suggestions in Airlabs by search query. |

### Flight

| Action | Method | Description |
| --- | --- | --- |
| [Get Flight Information](actions/get-flight-information.md) | GET | Retrieves current flight information from Airlabs. |
| [List Real-Time Flights](actions/list-real-time-flights.md) | GET | Retrieves real-time flight data from Airlabs. |

### Flight Alert Listener

| Action | Method | Description |
| --- | --- | --- |
| [Create Flight Alert Listener](actions/create-flight-alert-listener.md) | POST | Creates a flight alert listener in Airlabs. |
| [Delete Flight Alert Listener](actions/delete-flight-alert-listener.md) | DELETE | Deletes a flight alert listener from Airlabs. |
| [List Flight Alert Listeners](actions/list-flight-alert-listeners.md) | GET | Retrieves flight alert listeners from Airlabs. |

### Flight Alert Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Flight Alert Webhook History](actions/list-flight-alert-webhook-history.md) | GET | Retrieves flight alert webhook history from Airlabs. |

### Flight Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET | Retrieves airline route data from Airlabs. |

### Flight Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Flight Schedules](actions/list-flight-schedules.md) | GET | Retrieves upcoming flight schedules from Airlabs. |

### Nearby Airport

| Action | Method | Description |
| --- | --- | --- |
| [Find Nearby Airports](actions/find-nearby-airports.md) | GET | Finds nearby airports in Airlabs by coordinates. |

### Tax Code

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Codes](actions/list-tax-codes.md) | GET | Retrieves airline tax codes from Airlabs. |

### Time Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zone records from Airlabs. |

