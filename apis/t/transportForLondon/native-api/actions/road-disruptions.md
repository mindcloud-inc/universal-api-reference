# Get Road Disruptions with Transport for London

Retrieves road disruptions for selected roads in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Road/:ids/Disruption`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Road Disruptions](https://api.tfl.gov.uk/swagger/ui/index.html#!/Road/Road_Disruption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated TfL road IDs, such as A1,A2. |
