# Get Line Disruptions with Transport for London

Retrieves disruptions for selected lines in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/:ids/Disruption`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Line Disruptions](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Disruption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated TfL line IDs, such as victoria,circle. |
