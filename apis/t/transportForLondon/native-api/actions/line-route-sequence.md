# Get Line Route Sequence with Transport for London

Retrieves a line route sequence from Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/:id/Route/Sequence/:direction`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Line Route Sequence](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_RouteSequence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Single TfL line ID, such as victoria. |
| `direction` | path | `string` | yes | Direction of travel: inbound, outbound, or all. |
