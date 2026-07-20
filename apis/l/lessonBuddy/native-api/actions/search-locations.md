# Search Locations with LessonBuddy

Finds locations in LessonBuddy near an address.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/location/locations/search`
- **Base URL:** `https://api.lessonbuddy.com`
- **Official documentation:** [Search Locations](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Address string used for location search. |
| `distance` | body | `number` | yes | Distance for the location search. |
