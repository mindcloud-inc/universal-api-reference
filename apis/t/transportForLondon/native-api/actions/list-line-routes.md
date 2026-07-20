# List Line Routes with Transport for London

Retrieves line routes from Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/Route`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [List Line Routes](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceTypes` | query | `string` | no | Optional comma-separated service types. TfL supports Regular and Night. |
