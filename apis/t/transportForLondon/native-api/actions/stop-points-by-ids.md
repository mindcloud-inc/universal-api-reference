# Get Stop Points By IDs with Transport for London

Retrieves stop points by ID from Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/StopPoint/:ids`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Get Stop Points By IDs](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Comma-separated stop point IDs. TfL supports up to about 20. |
