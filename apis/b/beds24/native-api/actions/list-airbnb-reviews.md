# List Airbnb Reviews with Beds24

Retrieves Airbnb guest reviews from Beds24.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/airbnb/reviews`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Airbnb Reviews](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | query | `number` | yes | Beds24 room ID whose Airbnb reviews should be listed. |
