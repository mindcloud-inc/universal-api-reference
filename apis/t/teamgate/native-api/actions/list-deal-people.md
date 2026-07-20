# List Deal People with Teamgate

Retrieves people for a deal in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals/:deal_id/people`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [List Deal People](https://developers.teamgate.com/#eeb59e67-b8a4-4abc-92ad-dcd72ae69d3f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Deal ID whose linked people should be listed. |
