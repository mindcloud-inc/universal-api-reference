# List Room Offers with Beds24

Retrieves room offers from Beds24 by stay criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/rooms/offers`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Room Offers](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arrival` | query | `string` | yes | Offer search arrival date in YYYY-MM-DD format. |
| `departure` | query | `string` | yes | Offer search departure date in YYYY-MM-DD format. |
| `numAdults` | query | `number` | yes | Number of adults for the offer search. |
