# Search Google Flights with HasData

Retrieves Google Flights results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google/flights`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google Flights](https://docs.hasdata.com/apis/google-travel/flights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arrivalId` | query | `string` | yes | Arrival airport IATA code or location kgmid. |
| `departureId` | query | `string` | yes | Departure airport IATA code or location kgmid. |
| `outboundDate` | query | `string` | yes | Outbound travel date in YYYY-MM-DD format. |
| `returnDate` | query | `string` | no | Return travel date in YYYY-MM-DD format. |
| `type` | query | `string` | no | Flight type such as roundTrip or oneWay. |
