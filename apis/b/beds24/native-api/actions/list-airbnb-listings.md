# List Airbnb Listings with Beds24

Retrieves Airbnb listings from Beds24 by Airbnb user ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/airbnb/listings`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Airbnb Listings](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airbnbUserId` | query | `string` | yes | Connected Airbnb user ID to list listings for. |
