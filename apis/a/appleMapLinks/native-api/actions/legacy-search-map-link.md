# Legacy Search Map Link with Apple Map Links

Searches Apple Maps using the legacy map link.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Legacy Search Map Link](https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Legacy map search query. Apple notes `q=*` is not supported. |
