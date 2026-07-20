# Geocode By Place with Ambee

Retrieves location coordinates in Ambee by place name.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/by-place`
- **Base URL:** `https://api.ambeedata.com`
- **Official documentation:** [Geocode By Place](https://docs.ambeedata.com/apis/location#geocoding-placewise)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `place` | query | `string` | yes | Name of the location to search. |
