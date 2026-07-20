# Search Google Flights with ScrapingDog

Retrieves Google Flights search results through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_flights`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Search Google Flights](https://docs.scrapingdog.com/google-flights-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arrival_id` | query | `string` | yes | Arrival airport code or location identifier. |
| `departure_id` | query | `string` | yes | Departure airport code or location identifier. |
| `outbound_date` | query | `string` | yes | Outbound travel date in YYYY-MM-DD format. |
