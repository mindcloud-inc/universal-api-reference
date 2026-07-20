# Get Household with Planning Center

Retrieves a household from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/households/:id`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Get Household](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The household id. |
| `include` | query | `string` | no | Include associated people in the response. |
