# Create Household with Planning Center

Creates a new household in Planning Center.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/v2/households`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Create Household](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for the request payload. |
| `include` | query | `string` | no | Include associated people in the response. |
