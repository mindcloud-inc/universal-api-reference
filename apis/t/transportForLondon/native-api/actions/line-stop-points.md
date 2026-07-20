# List Line Stop Points with Transport for London

Retrieves stop points served by a line in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/:id/StopPoints`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [List Line Stop Points](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_StopPoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Single TfL line ID, such as victoria. |
