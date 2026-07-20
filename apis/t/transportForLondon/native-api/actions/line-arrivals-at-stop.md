# Get Line Arrivals At Stop with Transport for London

Retrieves line arrivals at a stop in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/:ids/Arrivals/:stopPointId`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Line Arrivals At Stop](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Arrivals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated TfL line IDs, such as victoria,circle. |
| `stopPointId` | path | `string` | yes | TfL stop point ID, such as 940GZZLUASL. |
