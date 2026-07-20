# Get Closest Locations with LessonBuddy

Finds locations in LessonBuddy by distance from coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/location/locations/closest/:latitude/:longitude/:radius`
- **Base URL:** `https://api.lessonbuddy.com`
- **Official documentation:** [Get Closest Locations](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | path | `number` | yes | Latitude for the center point. |
| `longitude` | path | `number` | yes | Longitude for the center point. |
| `radius` | path | `number` | yes | Search radius around the latitude and longitude. |
