# Get Road Status with Transport for London

Retrieves road status for selected roads in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/Road/:ids/Status`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Road Status](https://api.tfl.gov.uk/swagger/ui/index.html#!/Road/Road_Status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated TfL road IDs, such as A1,A2. |
