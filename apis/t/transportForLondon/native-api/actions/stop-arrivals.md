# Get Stop Arrivals with Transport for London

Retrieves arrivals for a stop in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/StopPoint/:id/Arrivals`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Stop Arrivals](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Arrivals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TfL stop point ID, such as 940GZZLUASL. |
