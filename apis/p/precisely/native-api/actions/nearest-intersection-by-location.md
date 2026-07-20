# Nearest Intersection By Location with Precisely

Retrieves the nearest intersection from Precisely by location.

## Endpoint

- **Method:** `GET`
- **Path:** `/streets/v1/intersection/bylocation`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Nearest Intersection By Location](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Streets/ByLocation/major_intersections_by_location.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude for the target point. |
| `longitude` | query | `number` | yes | Longitude for the target point. |
